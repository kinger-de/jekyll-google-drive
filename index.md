---
layout: default
header:
  image_fullwidth: unsplash-outback.jpg
permalink: /index.html
homepage: true
# mediaplayer: true
# breadcrumb: true -- re enable this once these are implimented in sheets
googlesheetpull: true
googlesheetlayout: home
---

<div class="row t30 b30">
    <form>
        <div class="editor large-12 columns" style="display: none">
            <div class="large-12 columns">
                <button type="button" style="width:100%" class="note button radius" id="closeeditor-button" onclick="close_current_editor(event)">
                    Close editor
                </button>
            </div>
            <div id="authorize-div" style="display: none">
                <div class="large-12 columns">
                    <button type="button" style="width:100%" class="note button radius" id="authorize-button" onclick="handleAuthClick(event)">
                        CLICK ME <br>
                        Before you can edit this page you need to authorise this
                        website to edit your personal Google Sheets with a Google 
                        account that has been given access to the website 
                        spreadsheet.
                    </button>
                </div>
            </div>
            <div id="editor-div" style="display: none">
                <div class="large-12 columns">
                    <textarea id="tinemce_page_editor" style="height:250" class="page_editor"></textarea>
                </div>
            </div>
            <div id="noaccess-div" style="display: none">
                <div data-alert class="alert-box info radius">
                    When attempting to edit the 
                    <a href="https://docs.google.com/spreadsheets/d/{{ site.google_sheet_id }}/edit">website spreadsheet</a>
                    an error was returned. Does your currently signed in Google 
                    account have sufficient permissions to edit the
                    <a href="https://docs.google.com/spreadsheets/d/{{ site.google_sheet_id }}/edit">website spreadsheet</a>? 
                    If not and you believe you should please 
                    <a href="/?page=aboutus-contact">contact us</a>.
                </div>
            </div>
        </div>
    </form>
</div>

<div class="google-sheet-layout"></div>

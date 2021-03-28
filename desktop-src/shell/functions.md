---
description: In diesem Abschnitt werden die Windows-Shellfunktionen beschrieben.
title: Shellfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c8e31bdaac8ec581504326c17d5d37012dd019d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994718"
---
# <a name="shell-functions"></a>Shellfunktionen

\[Diese Funktion ist nicht mehr implementiert.\]

In diesem Abschnitt werden die Windows-Shellfunktionen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="intsafe-h-functions-bumper.md">Intafe. h-Funktionen</a><br/></td>

</tr>
<tr class="even">
<td><a href="library-functions-bumper.md">Bibliotheksfunktionen</a><br/></td>

</tr>
<tr class="odd">
<td><a href="path-functions.md">Path-Funktionen</a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>Assockreateforclasses</strong></a><br/></td>
<td>Ruft ein Objekt ab, das eine <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>iqueryassociations</strong></a> -Schnittstelle implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>Assocgetdetailsofpropkey</strong></a><br/></td>
<td>Ruft den Wert für einen angegebenen Eigenschafts Schlüssel mithilfe der Datei Zuordnungs Informationen ab, die von den <a href="nse-works.md">Namespace Erweiterungen</a>bereitgestellt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a><br/></td>
<td>Erstellt ein Kontextmenü für eine ausgewählte Gruppe von Datei Ordner Objekten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>Cishutdown</strong></a><br/></td>
<td>Beendet den inhaltsindexer und schließt alle geöffneten Kataloge. <br/>
<blockquote>
[!Note]<br />
Diese Funktion wird ab Windows 8 nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>Commandlineumargvw</strong></a><br/></td>
<td>Analysiert eine Unicode-Befehlszeilen Zeichenfolge und gibt ein Array von Zeigern zu den Befehlszeilen Argumenten zusammen mit der Anzahl derartiger Argumente auf eine Weise zurück, die den standardmäßigen C-Lauf Zeitwerten <em>argv</em> und <em>argc</em> ähnelt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a><br/></td>
<td>Fungiert als Einstiegspunkt für eine System Steuerungsanwendung. Dies ist eine Bibliotheks definierte Rückruffunktion.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>"Kreateappcontainerprofile"</strong></a><br/></td>
<td>Erstellt ein pro-Benutzer-Profil pro App für Windows Store-Apps.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>"Kreateumgebblock"</strong></a><br/></td>
<td>Ruft die Umgebungsvariablen für den angegebenen Benutzer ab. Dieser Block kann dann <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>an die Funktion</strong></a> "-Funktion" von "|" übergeben werden.<br/></td>
</tr>
<tr class="even">
<td><a href="createmrulist.md"><strong>"Kreatemrulistw"</strong></a><br/></td>
<td>Erstellt eine neue Liste der zuletzt verwendeten (MRU).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>"Kreateprofile"</strong></a><br/></td>
<td>Erstellt ein neues Benutzerprofil.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>Defscreensaverproc</strong></a><br/></td>
<td>Bietet Standard Verarbeitung für alle Nachrichten, die von einer Bildschirmschoner-Anwendung nicht verarbeitet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>Defsubclassproc</strong></a><br/></td>
<td>Ruft den nächsten Handler in der Unterklassen Kette eines Fensters auf. Der letzte Handler in der Unterklassen Kette Ruft die ursprüngliche Fenster Prozedur für das Fenster auf.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>Deleteappcontainerprofile</strong></a><br/></td>
<td>Löscht das angegebene Profil pro Benutzer und pro app.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a><br/></td>
<td>Löscht das Benutzerprofil und alle Benutzer bezogenen Einstellungen vom angegebenen Computer. Der Aufrufer muss über Administratorrechte verfügen, um das Profil eines Benutzers löschen zu können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>Destroyumgebblock</strong></a><br/></td>
<td>Gibt Umgebungsvariablen frei, die von der Funktion " <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>kreateenvironment Block</strong></a> " erstellt wurden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>Deriveappcontainersidfromappcontainername</strong></a><br/></td>
<td>Ruft die SID des angegebenen Profils ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>Deriverestrictedappcontainersidfromappcontainersidandrestrictedname</strong></a><br/></td>
<td>Deriverestrictedappcontainersidfromappcontainersidandrestrictedname ist für die zukünftige Verwendung reserviert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>Dllgetversionproc</em></a><br/></td>
<td>Wird von vielen Windows Shell-DLLs implementiert, damit Anwendungen dll-spezifische Versionsinformationen erhalten können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a><br/></td>
<td>Registriert, ob ein Fenster gelöschte Dateien akzeptiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>Dragfinish</strong></a><br/></td>
<td>Gibt Arbeitsspeicher frei, der vom System zum Übertragen von Dateinamen an die Anwendung zugeordnet wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>Dragqueryfile</strong></a><br/></td>
<td>Ruft die Namen gelöschter Dateien ab, die sich aus einem erfolgreichen Drag & Drop-Vorgang ergeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>Dragquerypoint</strong></a><br/></td>
<td>Ruft die Position des Mauszeigers zu dem Zeitpunkt ab, zu dem eine Datei während eines Drag & Drop-Vorgangs abgelegt wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>Duplialisieicon</strong></a><br/></td>
<td>Erstellt ein Duplikat eines angegebenen Symbols.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>Expandumgebstringsforuser</strong></a><br/></td>
<td>Erweitert die Quell Zeichenfolge mit dem Umgebungsblock, der für den angegebenen Benutzer eingerichtet wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a><br/></td>
<td>Ruft ein Handle für ein Symbol ab, das als Ressource in einer Datei oder als Symbol in der zugeordneten ausführbaren Datei einer Datei gespeichert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a><br/></td>
<td>Ruft ein Handle für ein Symbol aus der angegebenen ausführbaren Datei, dll oder Symbol Datei ab. <br/> Verwenden Sie die <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>extractienex</strong></a> -Funktion, um ein Array von Handles für große oder kleine Symbole abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>Extracticonfiguration</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>extractienex</strong></a> -Funktion erstellt ein Array von Handles für große oder kleine Symbole, die aus der angegebenen ausführbaren Datei, dll oder Symbol Datei extrahiert werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="fileiconinit.md"><strong>"Fleiconfiguration"</strong></a><br/></td>
<td>Initialisiert oder initialisiert die System Abbild Liste neu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>Findexecutable</strong></a><br/></td>
<td>Ruft den Namen des-und-Handles für die ausführbare Datei (. exe) ab, die einer bestimmten Dokument Datei zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>Freeconfirmconflictitem</strong></a><br/></td>
<td>Gibt die Ressourcen frei, die für eine <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> Struktur reserviert wurden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>Freeidlistarray</strong></a><br/></td>
<td>Gibt den von einem Zeiger verwendeten Arbeitsspeicher auf ein PIDL-Listen Array (Item Identifier List) frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>Freeidlistarraychild</strong></a><br/></td>
<td>Gibt den Speicherplatz für das Array von Zeigern auf untergeordnete Element-IDs frei. Dadurch werden sowohl der PITEMID_CHILDs innerhalb des Arrays als auch das Array selbst freigegeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>Freeidlistarrayfull</strong></a><br/></td>
<td>Gibt den Speicherplatz für das PIDL-Array frei. Dadurch werden sowohl der PIDLIST_ABSOLUTEs innerhalb des Arrays als auch das Array selbst freigegeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a><br/></td>
<td>Gibt die zugewiesenen Felder im Ergebnis aus <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>iknownfolder:: getfolderdefinition</strong></a>frei.<br/></td>
</tr>
<tr class="even">
<td><a href="freemrulist.md"><strong>Freemrulist</strong></a><br/></td>
<td>Gibt das der MRU-Liste zugeordnete Handle frei und schreibt zwischengespeicherte Daten in die Registrierung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>Getallusersprofiledirectory</strong></a><br/></td>
<td>Ruft den Pfad zum Stammverzeichnis des Verzeichnisses ab, das die Programm Daten enthält, die von allen Benutzern gemeinsam genutzt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>Getappcontainerfolderpath</strong></a><br/></td>
<td>Ruft den Pfad des Ordners der lokalen app-Daten für den angegebenen app-Container ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>Getappcontainerregistrylocation</strong></a><br/></td>
<td>Ruft den Speicherort des Registrierungs Speichers ab, der einem App-Container zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>Getkontratdelegatewindow</strong></a><br/></td>
<td>Ruft ein Fenster ab, das als Delegat für das primäre Vordergrund Fenster einer APP festgelegt wurde, um das delegatfenster den Verträgen der APP zuzuordnen. Verwenden Sie diese Funktion, wenn Sie Entwickler sind, die eine Windows Store-App in nativem C++ schreiben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>Getcurrentprocessexplicitappusermodelid</strong></a><br/></td>
<td>Ruft die Anwendungs definierte, explizite Anwendungs Benutzer Modell-ID (appusermodelid) für den aktuellen Prozess ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a><br/></td>
<td>Ruft den Pfad zum Stamm des Standardbenutzer Profils ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>Getdpiforshelluicomponent</strong></a><br/></td>
<td>Ruft die dpi-Punkte pro Zoll (dpi) ab, die von einem <a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a> basierend auf dem aktuellen Skalierungsfaktor und <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>belegt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>Getmenucontexthelpid</strong></a><br/></td>
<td>Ruft den dem angegebenen Menü zugeordneten Hilfe Kontext Bezeichner ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a><br/></td>
<td>Ruft den Pfad zum Stammverzeichnis ab, in dem Benutzerprofile gespeichert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>Getprofiletype</strong></a><br/></td>
<td>Ruft den Typ des Profils ab, das für den aktuellen Benutzer geladen wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>Getscalefactor fordevice</strong></a><br/></td>
<td>Ruft den bevorzugten Skalierungsfaktor für ein Anzeigegerät ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>Getscalefactor formonitor</strong></a><br/></td>
<td>Ruft den Skalierungsfaktor eines bestimmten Monitors ab. Diese Funktion ersetzt <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>getscalefactorfordevice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>Getuserprofiledirectory</strong></a><br/></td>
<td>Ruft den Pfad zum Stammverzeichnis des angegebenen Benutzerprofils ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>Getwindowcontexthelpid</strong></a><br/></td>
<td>Ruft ggf. den dem angegebenen Fenster zugeordneten Hilfe Kontext Bezeichner ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>Getwindowsubclass</strong></a><br/></td>
<td>Ruft die Verweis Daten für den angegebenen Windows-Unterklassen Rückruf ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>Idlistcontaineriskonsistente</strong></a><br/></td>
<td>Überprüft, ob die Containerstruktur einer idlist gültig ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>Ilappendid</strong></a><br/></td>
<td>Fügt eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur an eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur an oder fügt Sie an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>Ilclone</strong></a><br/></td>
<td>Klont eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>Ilclonechild</strong></a><br/></td>
<td>Klont eine untergeordnete <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>Ilclonefirst</strong></a><br/></td>
<td>Klont die erste <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur in einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>Ilclonefull</strong></a><br/></td>
<td>Klont eine vollständige oder absolute, <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>Ilcombine</strong></a><br/></td>
<td>Kombiniert zwei <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Strukturen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>Ilkreatefrompath</strong></a><br/></td>
<td>Gibt die <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur zurück, die einem angegebenen Dateipfad zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>Ilfindchild</strong></a><br/></td>
<td>Bestimmt, ob eine angegebene <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur das untergeordnete Element einer anderen <strong>itemittel List</strong> -Struktur ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>Ilfindlastid</strong></a><br/></td>
<td>Gibt einen Zeiger auf die letzte <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur in einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>Nicht verfügbar</strong></a><br/></td>
<td>Gibt eine von der Shell zugeordnete <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>Ilgetnext</strong></a><br/></td>
<td>Ruft die nächste <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur in einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>Ilgetsize</strong></a><br/></td>
<td>Gibt die Größe einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur in Bytes zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>Ilisausgerichtet</strong></a><br/></td>
<td>Überprüft, ob eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>konstanteniteferlist</strong></a> an einer Zeiger Grenze ausgerichtet ist, bei der es sich um ein <strong>DWORD</strong> -Element in 32-Bit-Architekturen und ein <strong>QWORD</strong> in 64-Bit-Architekturen handelt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>Ilischild</strong></a><br/></td>
<td>Überprüft, ob es sich bei einer PIDL um eine untergeordnete PIDL handelt, bei der es sich um eine PIDL mit genau einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a>handelt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>Ility</strong></a><br/></td>
<td>Überprüft, ob eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur leer ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>Ilisequal</strong></a><br/></td>
<td>Testet, ob zwei <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittellist</strong></a> -Strukturen bei einem binären Vergleich gleich sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>Ilisparent</strong></a><br/></td>
<td>Testet, ob eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur das übergeordnete Element einer anderen <strong>itemittel List</strong> -Struktur ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>Ilnext (PCUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Ruft die nächste <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur in einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>Ilnext (PUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Ruft die nächste <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur in einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>Ilremovelastid</strong></a><br/></td>
<td>Entfernt die letzte <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>shitemid</strong></a> -Struktur aus einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemidlist</strong></a> -Struktur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>Ilsavedestream</strong></a><br/></td>
<td>Speichert eine <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittellist</strong></a> -Struktur in einem Stream.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>Ilskip (PCUIDLIST_RELATIVE, uint)</strong></a><br/></td>
<td>Überspringt eine angegebene Anzahl von Bytes in einer Konstanten, nicht ausgerichteten, relativen <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>Ilskip (PUIDLIST_RELATIVE, uint)</strong></a><br/></td>
<td>Überspringt eine angegebene Anzahl von Bytes in einer nicht ausgerichteten, relativen <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>Inetisoffline</strong></a><br/></td>
<td>Bestimmt, ob das System mit dem Internet verbunden ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>Initnetworkaddresscontrol</strong></a><br/></td>
<td>Initialisiert die Fenster Klasse der Netzwerk Adress Steuerung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a><br/></td>
<td>Lädt das Profil des angegebenen Benutzers. Das Profil kann ein <a href="local-user-profiles.md">Lokales Benutzerprofil</a> oder ein <a href="roaming-user-profiles.md">Roamingbenutzerprofil</a>sein.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>Mimeassociationdialog</strong></a><br/></td>
<td>Führt das Dialogfeld nicht registrierte MIME-Inhaltstyp aus.<br/>
<blockquote>
[!Note]<br />
Windows XP Service Pack 2 (SP2) oder höher: Diese Funktion wird nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>Pathmakeuniquename</strong></a><br/></td>
<td>Erstellt einen eindeutigen Pfadnamen aus einer Vorlage.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>Pathyetanothermakeuniquename</strong></a><br/></td>
<td>Erstellt auf der Grundlage eines vorhandenen Datei namens einen eindeutigen Dateinamen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>Registerappstatuechangenotifizierung</strong></a><br/></td>
<td>Ermöglicht einer APP, eine Rückruffunktion zu registrieren, über die Sie benachrichtigt werden kann, dass die Bibliothek in den Status "angehalten" versetzt wird. Diese Informationen können von der APP verwendet werden, um alle notwendigen Vorgänge auszuführen, z. b. die Beibehaltung des Zustands, die zu diesem Zeitpunkt durchgeführt werden sollen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>Registerdialogclasses</strong></a><br/></td>
<td>Registriert alle nicht standardmäßigen Fenster Klassen, die für das Konfigurations Dialogfeld eines Bildschirmschoners erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>Registerscalechangeevent</strong></a><br/></td>
<td>Registriert für ein Ereignis, das ausgelöst wird, wenn die Skala möglicherweise geändert wurde. Diese Funktion ersetzt <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>registerscalechangenotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>Registerscalechangenotifications</strong></a><br/></td>
<td>Registriert ein Fenster, um Rückrufe zu empfangen, wenn sich die Skalierungsinformationen ändern.<br/>
<blockquote>
[!Note]<br />
Diese Funktion wird ab Windows 8.1 nicht unterstützt. Verwenden Sie stattdessen <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>registerscalechangeevent</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>Removewindowsubclass</strong></a><br/></td>
<td>Entfernt einen Unterklassen Rückruf aus einem Fenster.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>Revokescalechangenotifications</strong></a><br/></td>
<td>Widerruft die Registrierung eines Fensters und verhindert, dass Rückrufe empfangen werden, wenn die Skalierung von Informationen geändert wird.<br/>
<blockquote>
[!Note]<br />
Diese Funktion wird ab Windows 8.1 nicht unterstützt. Verwenden Sie stattdessen <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>unregisterscalechangeevent</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>Screensaverkonfiguriredialog</strong></a><br/></td>
<td>Empfängt Nachrichten, die an das Konfigurations Dialogfeld eines Bildschirmschoners gesendet werden. Ein Bildschirmschoner, der die Benutzerkonfiguration ermöglicht, muss diese Funktion definieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>Screensaverproc</strong></a><br/></td>
<td>Empfängt Nachrichten, die an das angegebene Bildschirmschoner Fenster gesendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>Setverhütdelegatewindow</strong></a><br/></td>
<td>Ordnet ein App-Fenster außer dem primären Vordergrund Fenster mit den Verträgen einer APP zu. Verwenden Sie diese Funktion, wenn Sie Entwickler sind, die eine Windows Store-App in nativem C++ schreiben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Gibt eine eindeutige, von der Anwendung definierte appusermodelid an, die den aktuellen Prozess auf der Taskleiste identifiziert. Mit diesem Bezeichner kann eine Anwendung die zugeordneten Prozesse und Fenster unter einer einzelnen Task leisten Schaltfläche gruppieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>Setmenucontexthelpid</strong></a><br/></td>
<td>Ordnet einem Menü einen Hilfe Kontext Bezeichner zu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>Setwindowcontexthelpid</strong></a><br/></td>
<td>Ordnet dem angegebenen Fenster einen Hilfe Kontext Bezeichner zu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>Setwindowsubclass</strong></a><br/></td>
<td>Installiert oder aktualisiert einen Windows-Unterklassen Rückruf.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>"Shaddtor ecentdocs"</strong></a><br/></td>
<td>Benachrichtigt das System, dass auf ein Element zugegriffen wurde, um die zuletzt und am häufigsten verwendeten Elemente zu überwachen. Diese Funktion kann auch verwendet werden, um alle Verwendungs Daten zu löschen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a><br/></td>
<td>Sendet eine appbar-Meldung an das System.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>Shassocenumhandlers</strong></a><br/></td>
<td>Gibt ein Enumerationsobjekt für einen angegebenen Satz von Dateinamen-Erweiterungs Handlern zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>Shassocenumhandlersforprotocolbyapplication</strong></a><br/></td>
<td>Ruft eine Enumerationsschnittstelle ab, die Zugriff auf Handler bereitstellt, die einem angegebenen Protokoll zugeordnet sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>Shbindeinfolderidlistparent</strong></a><br/></td>
<td>Wenn ein in der Form eines Ordners angegebener Shell-Namespace Element und eine Element Bezeichner-Liste relativ zu diesem Ordner angegeben ist, bindet diese Funktion an das übergeordnete Element des Namespace Elements und gibt optional einen Zeiger auf die endgültige Komponente der Element Bezeichner-Liste zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>Shbindeinfolderidlistklammer</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>shbindtefolderidlistparent</strong></a> -Funktion, indem dem Aufrufer ermöglicht wird, einen Bindungs Kontext anzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>Shbindjeobject</strong></a><br/></td>
<td>Ruft ein angegebenes-Objekt mithilfe der Shell-Namespace <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindTo Object</strong></a> -Methode ab und bindet es an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>Shbindtoparent</strong></a><br/></td>
<td>Nimmt einen Zeiger auf eine voll qualifizierte elementbezeichnerliste (PIDL) und gibt einen angegebenen Schnittstellen Zeiger für das übergeordnete Objekt zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>Shbrowsforfolder</strong></a><br/></td>
<td>Zeigt ein Dialogfeld an, in dem der Benutzer einen Shellordner auswählen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a><br/></td>
<td>Sperrt den gemeinsam genutzten Arbeitsspeicher, der einem shelländerungs-Benachrichtigungs Ereignis zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a><br/></td>
<td>Entsperrt gemeinsam genutzten Speicher für eine Änderungs Benachrichtigung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>Shchangenotifizieren</strong></a><br/></td>
<td>Benachrichtigt das System über ein Ereignis, das von einer Anwendung ausgeführt wurde. Eine Anwendung sollte diese Funktion verwenden, wenn Sie eine Aktion ausführt, die sich möglicherweise auf die Shell auswirkt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>Shchangenotifyderegiester</strong></a><br/></td>
<td>Hebt die Registrierung des Fenster Prozesses des Clients beim Empfang von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>shchangenotify</strong></a> -Nachrichten auf.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>Shchangenotifyregister</strong></a><br/></td>
<td>Registriert ein Fenster für den Empfang von Benachrichtigungen aus dem Dateisystem oder der Shell, wenn das Dateisystem Benachrichtigungen unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>Shchangenotifyregisterthread</strong></a><br/></td>
<td>Aktiviert das asynchrone registrieren und Aufheben der Registrierung eines Threads.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>Shkreateassociationregistration</strong></a><br/></td>
<td>Erstellt ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>iapplicationassociationregistration</strong></a> -Objekt auf der Grundlage der Lager Implementierung der von Windows bereitgestellten-Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>Shkreatedataobject</strong></a><br/></td>
<td>Erstellt ein Datenobjekt in einem übergeordneten Ordner.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>Shkreatedefaultcontextmenu</strong></a><br/></td>
<td>Erstellt ein-Objekt, das die standardmäßige Kontextmenü Implementierung der Shell darstellt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>Shkreatedefaultextracticon</strong></a><br/></td>
<td>Erstellt einen Standard Symbol Extraktor, dessen Standardwerte über die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>idefaultextracticonfiguration</strong></a> -Schnittstelle weiter konfiguriert werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>Shkreatedefaultpropertiesop</strong></a><br/></td>
<td>Erstellt einen Datei Vorgang, der die Standardeigenschaften für das shellelement festlegt, die noch nicht festgelegt wurden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>Shkreateitemfromittlerlist</strong></a><br/></td>
<td>Erstellt und initialisiert ein shellelementobjekt aus einem PIDL. Das resultierende shellelementobjekt unterstützt die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>Shkreateitemfromparser-Name</strong></a><br/></td>
<td>Erstellt und initialisiert ein Shellelementobjekt aus einem Analysenamen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>Shkreateitemfromrelativename</strong></a><br/></td>
<td>Erstellt und initialisiert ein shellelementobjekt aus einem relativen Elementnamen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>Shkreateiteminknownfolder</strong></a><br/></td>
<td>Erstellt ein shellelementobjekt für eine einzelne Datei, die in einem bekannten Ordner vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>Shkreateitemwithparent</strong></a><br/></td>
<td>Erstellen Sie ein shellelement, wenn ein übergeordneter Ordner und eine untergeordnete Element-ID angegeben sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>Shkreateshellfolderview</strong></a><br/></td>
<td>Erstellt eine neue Instanz des standardshellordneransichtsobjekt (defview).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>Shkreateshellfolderviewex</strong></a><br/></td>
<td>Erstellt eine neue Instanz des standardshellordneransichtsobjekt. Es wird empfohlen, dass Sie <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>shkreateshellfolderview</strong></a> anstelle dieser Funktion verwenden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>Shkreateshellitem</strong></a><br/></td>
<td>Erstellt ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekt. <br/>
<blockquote>
[!Note]<br />
Es wird empfohlen, anstelle dieser Funktion " <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>shfroateitemwithparent</strong></a> " oder " <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>shfroateitemfromittlerlist</strong></a> " zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>Shkreateshellitemarray</strong></a><br/></td>
<td>Erstellt ein shellelementarray-Objekt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>Shkreateshellitemarrayfromdataobject</strong></a><br/></td>
<td>Erstellt ein shellelementarray-Objekt aus einem Datenobjekt. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>Shfroateshellitemarrayfromitten Lists</strong></a><br/></td>
<td>Erstellt ein shellelementarray-Objekt aus einer Liste von <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Strukturen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>Shkreateshellitemarrayfromshellitem</strong></a><br/></td>
<td>Erstellt ein Array mit einem Element aus einem einzelnen shellelement.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>Shdefextracticon</strong></a><br/></td>
<td>Stellt einen Standard Handler zum Extrahieren eines Symbols aus einer Datei bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>Shdodragdrop</strong></a><br/></td>
<td>Führt einen Drag & Drop-Vorgang aus. Unterstützt die Erstellung von Drag-Source-Anforderungen bei Bedarf sowie das Ziehen von Bildern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a><br/></td>
<td>Sendet eine Meldung an den Statusbereich der Taskleiste.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a><br/></td>
<td>Ruft die Bildschirm Koordinaten des umgebenden Rechtecks eines Benachrichtigungs Symbols ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>Shellabout</strong></a><br/></td>
<td>Zeigt ein <strong>shellabout</strong> -Dialogfeld an.<br/></td>
</tr>
<tr class="even">
<td><a href="shellddeinit.md"><strong>Shellddeingeit</strong></a><br/></td>
<td>Registriert die shelldienste (shelldynamischer Datenaustausch) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a><br/></td>
<td>Führt einen Vorgang für eine angegebene Datei aus.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a><br/></td>
<td>Führt einen Vorgang für eine angegebene Datei aus.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>Shemptyrecyclebin</strong></a><br/></td>
<td>Leert den Papierkorb auf dem angegebenen Laufwerk.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>Shenumerateunlesermailaccounts</strong></a><br/></td>
<td>Listet die Benutzerkonten auf, für die ungelesene e-Mails vorhanden sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>Shevaluatesystemcommandtemplate</strong></a><br/></td>
<td>Erzwingt eine strikte Validierung von Parametern, die in einem <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>aufrufungsprozess</strong></a> oder <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a><br/></td>
<td>Kopiert, verschiebt, benennt oder löscht ein Dateisystem Objekt. Diese Funktion wurde in Windows Vista durch <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>ersetzt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>Shfreenamemappings</strong></a><br/></td>
<td>Gibt ein Dateinamen-Mapping-Objekt frei, das von der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> -Funktion abgerufen wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>Shgetdatafromittellist</strong></a><br/></td>
<td>Ruft erweiterte Eigenschaften Daten aus einer relativen bezeichnerliste ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>Shgetdesktopfolder</strong></a><br/></td>
<td>Ruft die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> -Schnittstelle für den Desktop Ordner ab, der das Stammverzeichnis des Shell-Namespace ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>Shgetdiskfreespaceex</strong></a><br/></td>
<td>Ruft Informationen zum Speicherplatz für ein Datenträger Volume ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>Shgetdrivemedia</strong></a><br/></td>
<td>Gibt den Typ des Mediums im angegebenen Laufwerk zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>Shgetfileingefo</strong></a><br/></td>
<td>Ruft Informationen zu einem Objekt im Dateisystem ab, z. b. eine Datei, einen Ordner, ein Verzeichnis oder einen Laufwerks Stamm.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>Shgetfolderpathex</strong></a><br/></td>
<td>Ruft den vollständigen Pfad eines bekannten Ordners ab, der durch die <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>des Ordners identifiziert wird. Dadurch wird " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>shgetknownfolderpath</strong></a> " erweitert, indem Sie die anfängliche Größe des Zeichen folgen Puffers festlegen können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>Shgetitaroverlayindex</strong></a><br/></td>
<td>Gibt den Index des Überlagerungs Symbols in der System Abbild Liste zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>Shgetidlistfromuject</strong></a><br/></td>
<td>Ruft die PIDL eines Objekts ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>Shgetimagelist</strong></a><br/></td>
<td>Ruft eine Bildliste ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>Shgetinstanceexplorer</strong></a><br/></td>
<td>Ruft eine Schnittstelle ab, mit der gehostete Shellerweiterungen und andere Komponenten verhindern können, dass Ihr Host Prozess vorzeitig geschlossen wird. Der Host Prozess ist in der Regel Windows Explorer oder Windows Internet Explorer, aber diese Funktion kann auch von anderen Anwendungen verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>Shgetitemfromdataobject</strong></a><br/></td>
<td>Erstellt ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekt oder ein verknüpftes Objekt auf Grundlage eines durch ein <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>angegebenen Elements.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>Shgetitemfromuject</strong></a><br/></td>
<td>Ruft ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekt für ein-Objekt ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>Shgetknownfolderidlist</strong></a><br/></td>
<td>Ruft den Pfad eines bekannten Ordners als <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>Shgetknownfolderitem</strong></a><br/></td>
<td>Ruft ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekt ab, das einen bekannten Ordner darstellt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>Shgetknownfolderpath</strong></a><br/></td>
<td>Ruft den vollständigen Pfad eines bekannten Ordners ab, der durch die <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>des Ordners identifiziert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>Shgetlocalizedname</strong></a><br/></td>
<td>Ruft den lokalisierten Namen einer Datei in einem Shellordner ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>Shgetnamefroferlist</strong></a><br/></td>
<td>Ruft den anzeigen Amen eines durch seine idlist identifizierten Elements ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>Shgetnamefrompropertykey</strong></a><br/></td>
<td>Ruft den kanonischen Namen der Eigenschaft ab, wenn dessen <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a>angegeben ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>Shgetnewlinkinfo</strong></a><br/></td>
<td>Erstellt einen Namen für eine neue Verknüpfung basierend auf dem vorgeschlagenen Ziel der Verknüpfung. Diese Funktion erstellt nicht die Verknüpfung, sondern nur den Namen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>Shgetpathfromittlerlist</strong></a><br/></td>
<td>Konvertiert eine elementbezeichnerliste in einen Dateisystempfad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>Shgetpathfromittlerlistex</strong></a><br/></td>
<td>Konvertiert eine elementbezeichnerliste in einen Dateisystempfad. Diese Funktion erweitert " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>shgetpathfromittlerlist</strong></a> ", indem Sie die anfängliche Größe des Zeichen folgen Puffers festlegen und die unten aufgeführten Optionen deklarieren können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>Shgetsettings</strong></a><br/></td>
<td>Ruft die aktuellen shelloptionseinstellungen ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>Shgetstockiconinfo</strong></a><br/></td>
<td>Ruft Informationen zu System definierten shellsymbolen ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>Shgettemporarypropertyforitem</strong></a><br/></td>
<td>Ruft die temporäre Eigenschaft für das angegebene Element ab. Bei einer temporären Eigenschaft handelt es sich um einen Lese-/Schreibspeicher, der Eigenschaften nur für die Lebensdauer des <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekts enthält, anstatt wieder im Element abgelegt zu werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>Shgetunummailcount</strong></a><br/></td>
<td>Ruft die Anzahl der nicht gelesenen Nachrichten eines angegebenen Benutzers für beliebige oder alle e-Mail-Konten ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>Shismeleavailableoffline</strong></a><br/></td>
<td>Bestimmt, ob eine Datei oder ein Ordner für die Offline Verwendung verfügbar ist. Diese Funktion bestimmt außerdem, ob die Datei aus dem Netzwerk, aus dem lokalen Offlinedateien Cache oder aus beiden Speicherorten geöffnet werden würde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>Shloadinproc</strong></a><br/></td>
<td>Erstellt eine Instanz der angegebenen Objektklasse aus dem Kontext des Shellprozesses. <br/> <strong>Windows Vista</strong> und höher: Diese Funktion wurde deaktiviert und gibt E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>Shloadnonloadedikonoverlayidentifier</strong></a><br/></td>
<td>Signalisiert der Shell, dass beim nächsten Vorgang, der Überlagerungs Informationen erfordert, Symbol Überlagerungs Bezeichner geladen werden sollen, die bei der Erstellung fehlgeschlagen sind oder nicht für die Erstellung beim Start vorhanden waren. Bezeichner, die bereits geladen wurden, sind nicht betroffen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>Shlocalstraudup</strong></a><br/></td>
<td>Erstellt eine Kopie einer Zeichenfolge in neu zugewiesener Arbeitsspeicher.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>Shmultifileproperties</strong></a><br/></td>
<td>Zeigt ein zusammen geführtes Eigenschaften Blatt für einen Satz von Dateien an. Eigenschaftswerte, die allen Dateien gemeinsam sind, werden angezeigt, während unterschiedliche Eigenschaften die Zeichenfolge <strong>(mehrere Werte)</strong>anzeigen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>Shopenfolderandselectitems</strong></a><br/></td>
<td>Öffnet ein Windows-Explorer-Fenster, in dem die angegebenen Elemente in einem bestimmten Ordner ausgewählt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>Shopenwithdialog</strong></a><br/></td>
<td>Zeigt das Dialogfeld <strong>Öffnen mit an</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/showsharefolderui"><strong>Showsharefolderui</strong></a><br/></td>
<td>Zeigt die Registerkarte <strong>Ordner Freigabe</strong> auf der Eigenschaften Seite für den angegebenen Ordner an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>Shparametendisplayname</strong></a><br/></td>
<td>Übersetzt den anzeigen Amen eines Shell-Namespace Objekts in eine Element Bezeichner-Liste und gibt die Attribute des-Objekts zurück. Diese Funktion ist die bevorzugte Methode, um eine Zeichenfolge in eine PIDL zu konvertieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>Shpathprepareforwrite</strong></a><br/></td>
<td>Prüft, ob der Pfad vorhanden ist. Dies umfasst die erneute Einbindung zugeordneter Netzwerklaufwerke, das Anordnen von auswertbaren Medien Medien, das Erstellen der Pfade, das Aufrufen der zu formatierenden Medien und das Bereitstellen der entsprechenden Benutzeroberflächen, falls erforderlich. Lese-/Schreibberechtigungen für das Medium werden nicht geprüft.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>Shqueryrecyclebin</strong></a><br/></td>
<td>Ruft die Größe des Papierkorbs und die Anzahl der darin angegebenen Elemente für ein angegebenes Laufwerk ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>Shqueryusernotificationstate</strong></a><br/></td>
<td>Überprüft den Zustand des Computers für den aktuellen Benutzer, um zu bestimmen, ob das Senden einer Benachrichtigung angemessen ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>Shremovelocalizedname</strong></a><br/></td>
<td>Entfernt den lokalisierten Namen einer Datei in einem Shellordner.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>Shruncontrolpanel</strong></a><br/></td>
<td>Öffnet ein System Steuerungselement. <br/>
<blockquote>
[!Note]<br />
Diese Funktion wird ab Windows Vista nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>Shsetdefaultproperties</strong></a><br/></td>
<td>Wendet den Standardsatz von Eigenschaften für ein shellelement an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SH-tinstanceexplorer</strong></a><br/></td>
<td>Stellt eine Schnittstelle bereit, mit der gehostete Shellerweiterungen und andere Komponenten verhindern können, dass Ihr Host Prozess vorzeitig geschlossen wird. Der Host Prozess ist in der Regel Windows Explorer oder Internet Explorer, aber diese Funktion kann auch von anderen Anwendungen verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>Shsetknownfolderpath</strong></a><br/></td>
<td>Leitet einen bekannten Ordner an einen neuen Speicherort um.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>Shsetlocalizedname</strong></a><br/></td>
<td>Legt den lokalisierten Namen einer Datei in einem Shellordner fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>Shsettemporarypropertyforitem</strong></a><br/></td>
<td>Legt eine temporäre Eigenschaft für das angegebene Element fest. Eine temporäre Eigenschaft wird in einem Lese-/Schreibspeicher gespeichert, der Eigenschaften nur für die Lebensdauer des <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekts enthält, anstatt Sie zurück in das Element zu schreiben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>Shabtunummailcount</strong></a><br/></td>
<td>Speichert die Anzahl der ungelesenen Nachrichten des aktuellen Benutzers für ein bestimmtes e-Mail-Konto in der Registrierung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>Shtestumkenmitgliedschaft</strong></a><br/></td>
<td>Verwendet <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>checktokenmembership</strong></a> , um zu testen, ob das angegebene Token ein Mitglied der lokalen Gruppe mit der angegebenen RID ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>Shupdateimage</strong></a><br/></td>
<td>Benachrichtigt die Shell, dass sich ein Bild in der System Abbild Liste geändert hat.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>Softwareupdatemessagebox</strong></a><br/></td>
<td>Zeigt ein Standard Meldungs Feld an, das verwendet werden kann, um einen Benutzer zu benachrichtigen, dass eine Anwendung aktualisiert wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>Stgmakeuniquename</strong></a><br/></td>
<td>Erstellt einen eindeutigen Namen für einen Stream oder ein Speicher Objekt aus einer Vorlage.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>Die Schnittmenge</strong></a><br/></td>
<td>Sucht das erste Vorkommen einer Teil Zeichenfolge innerhalb einer Zeichenfolge. Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>Straume</strong></a><br/></td>
<td>Sucht das erste Vorkommen einer Teil Zeichenfolge innerhalb einer Zeichenfolge. Beim Vergleich wird die Groß-/Kleinschreibung beachtet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>Translateurl</strong></a><br/></td>
<td>Wendet allgemeine Übersetzungen auf eine angegebene URL-Zeichenfolge an und erstellt eine neue URL-Zeichenfolge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a><br/></td>
<td>Entlädt das Profil eines Benutzers, das von der <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> -Funktion geladen wurde. Der Aufrufer muss über Administratorrechte auf dem Computer verfügen. Weitere Informationen finden Sie im Abschnitt "Hinweise" der Funktion " <strong>LoadUserProfile</strong> ".<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>Unregisterappstatuechangenotifizierung</strong></a><br/></td>
<td>Bricht eine Änderungs Benachrichtigung ab, die über <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>registerappstatuechangenotifitifitifizierung</strong></a>registriert wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>Unregisterscalechangeevent</strong></a><br/></td>
<td>Hebt die Registrierung für das Ereignis der Skalierungs Änderung auf, das über <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>registerscalechangeevent</strong></a>registriert wird. Diese Funktion ersetzt <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>revokescalechangenotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>Urlassociationdialog</strong></a><br/></td>
<td>Ruft das Dialogfeld "nicht registriertes URL-Protokoll" auf. In diesem Dialogfeld kann der Benutzer eine Anwendung auswählen, die einem zuvor unbekannten Protokoll zugeordnet werden soll.<br/>
<blockquote>
[!Note]<br />
Windows XP SP2 oder höher: Diese Funktion wird nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>Winexecerror</strong></a><br/></td>
<td>Ruft den Fehlerwert ab, der generiert wird, wenn die <a href="/windows/win32/api/winbase/nf-winbase-winexec">winexec</a> -Funktion eine angegebene Anwendung nicht ausführen kann. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a><br/></td>
<td>Hiermit wird die Windows-Hilfe (Winhelp.exe) gestartet und zusätzliche Daten weitergeleitet, die die Art der von der Anwendung angeforderten Hilfe angeben.<br/></td>
</tr>
</tbody>
</table>



 

 

 

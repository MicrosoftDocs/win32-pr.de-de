---
description: In diesem Abschnitt werden die Windows-shellstrukturen beschrieben.
title: Shellstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bbda4cd81c3db2dff664b9d16d2db60aa8f12f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980801"
---
# <a name="shell-structures"></a>Shellstrukturen

In diesem Abschnitt werden die Windows-shellstrukturen beschrieben.

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
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>Aashellmenufilename</strong></a><br/></td>
<td>Eine Struktur variabler Größe, die Informationen über den Namen einer Menü Datei enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>Aashellmenuitem</strong></a><br/></td>
<td>Enthält Informationen zu einem Menü Element.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>Appbardata</strong></a><br/></td>
<td>Enthält Informationen zu einer appbar-Systemnachricht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>Appcategoryinfo</strong></a><br/></td>
<td>Stellt Informationen zur Anwendungskategorie zum Hinzufügen/Entfernen von Programmen in der Systemsteuerung bereit. Die <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>appcategoryinfolist</strong></a> -Struktur wird verwendet, um eine komplette Liste der Kategorien für einen Anwendungs Herausgeber zu erstellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>Appcategoryinfolist</strong></a><br/></td>
<td>Enthält eine Liste der unterstützten Anwendungskategorien von einem Anwendungs Herausgeber zum Hinzufügen/Entfernen von Programmen in der Systemsteuerung. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>Appinfodata</strong></a><br/></td>
<td>Stellt Informationen über eine veröffentlichte Anwendung im System Steuerungs Hilfsprogramm "Programme hinzufügen/entfernen" bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>Associationelement</strong></a><br/></td>
<td>Definiert Informationen, die von <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>assockreateforclasses</strong></a> verwendet werden, um eine <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>iqueryassociations</strong></a> -Schnittstelle für eine bestimmte Datei Zuordnung abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>Bandinfosfb</strong></a><br/></td>
<td>Enthält Informationen zu einem Ordner Band. Diese Struktur wird mit den Methoden <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>ishellfolderband:: getbandinfosfb</strong></a> und <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>ishellfolderband:: setbandinfosfb</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>Bandsiteinfo</strong></a><br/></td>
<td>Enthält Informationen zu einer Band Website. Diese Struktur wird mit der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>ibandsite:: getbandsiteinfo</strong></a> -Methode und der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>ibandsite:: setbandsiteinfo</strong></a> -Methode verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>Basebrowserdata</strong></a><br/></td>
<td>Enthält geschützte Member der Basisklasse. <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>Basebrowserdata</strong></a> definiert den Browser Zustand und wird mit <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2:: getbasebrowserdata</strong></a> und <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::P utbasebrowserdata</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>Borderbreiten</strong></a><br/></td>
<td>Definiert die Koordinaten der oberen linken und der unteren rechten Ecke eines Rahmen Rechtecks.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>Browseinfo</strong></a><br/></td>
<td>Enthält Parameter für die <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>shbrowsforfolder</strong></a> -Funktion und empfängt Informationen über den Ordner, der vom Benutzer ausgewählt wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>Enthält Kategorieinformationen. Eine Komponenten Kategorie ist eine Gruppe logisch verbundener Component Object Model (com)-Klassen, die eine gemeinsame Kategoriekennung (CATID) gemeinsam nutzen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>CIDA</strong></a><br/></td>
<td>Wird mit dem <a href="clipboard.md">CFSTR_SHELLIDLIST</a> -Zwischenablage Format verwendet, um den Zeiger auf eine Element Bezeichner-Liste (PIDL) eines oder mehrerer Shellnamespace-Objekte zu übertragen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>Definiert Spalten Informationen. Wird von Membern der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>Cminvokecommandinfo</strong></a><br/></td>
<td>Enthält Informationen, die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu:: InvokeCommand</strong></a> zum Aufrufen eines Kontextmenü Befehls benötigt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>Cminvokecommandinfoex</strong></a><br/></td>
<td>Enthält erweiterte Informationen zu einem Kontextmenü Befehl. Bei dieser Struktur handelt es sich um eine erweiterte Version von <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>cminvokecommandinfo</strong></a> , die die Verwendung von Unicode-Werten ermöglicht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>Wird generisch zum Filtern von Elementen verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>Zulieferern</strong></a><br/></td>
<td>Wird von Windows 2000 zum Speichern von Informationen zu einer Komponente verwendet. Diese Struktur ersetzt die <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> -Struktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>Componentsopt</strong></a><br/></td>
<td>Enthält die Desktop Element Optionen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>Comppos</strong></a><br/></td>
<td>Enthält Informationen über die Position und Größe einer Komponente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>Compstatueingefo</strong></a><br/></td>
<td>Wird von Windows 2000 zum Speichern von Informationen über den Status einer Komponente verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>Definiert die Konflikt Elementstruktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>Definiert die Struktur der Konflikt Ergebnisinformationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>Cplinfo</strong></a><br/></td>
<td>Enthält Ressourcen Informationen und einen von der Anwendung definierten Wert für ein Dialogfeld, das von einer System Steuerungsanwendung unterstützt wird. Die <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> -Funktion der System Steuerungsanwendung gibt diese Informationen als Antwort auf eine <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> Meldung an die Systemsteuerung zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a><br/></td>
<td>Enthält Details zu Anmelde Informationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a><br/></td>
<td>Beschreibt ein einzelnes Feld in den Anmelde Informationen. Beispielsweise eine Zeichenfolge oder ein Benutzer Image.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>Csfv</strong></a><br/></td>
<td>Wird mit der Funktion " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>shkreateshellfolderviewex</strong></a> " verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>Dient als Header für einige der zusätzlichen Datenstrukturen, die von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>ishelllinkdatalist</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>Defcontextmenu</strong></a><br/></td>
<td>Enthält Kontextmenü Informationen, die von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>shkreatedefaultcontextmenu</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>Delegateitemid</strong></a><br/></td>
<td>Wird von delegatenordnern anstelle einer standardmäßigen <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>itemittel List</strong></a> -Struktur verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>Detailsinfo</strong></a><br/></td>
<td>Enthält Detailinformationen für ein shellordnerelement. Wird mit der <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> Benachrichtigung verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>Dfmics</strong></a><br/></td>
<td>Enthält zusätzliche Argumente, die von <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>Dllversioninfo</strong></a><br/></td>
<td>Empfängt dll-spezifische Versionsinformationen. Sie wird mit der Funktion <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>dllgetversion</strong></a> verwendet. <br/>
<blockquote>
[!Note]<br />
Anstelle dieser Struktur können Sie die <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> -Struktur verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>Empfängt dll-spezifische Versionsinformationen. Sie wird mit der Funktion <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>dllgetversion</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>Dropdescription</strong></a><br/></td>
<td>Beschreibt das Bild und den begleitenden Text für ein Drop-Objekt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>Dropfiles</strong></a><br/></td>
<td>Definiert das <a href="clipboard.md">CF_HDROP</a> Zwischenablage Format. Bei den folgenden Daten handelt es sich um eine Double-NULL-terminierte Liste von Dateinamen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>Enthält einen zusätzlichen, von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>ishelllinkdatalist</strong></a>verwendeten Datenblock. Sie enthält die Windows Installer-ID des Links.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>Speichert Informationen über den Status der Shellverbindung. Diese Struktur wird für zusätzliche Datenabschnitte verwendet, die mit EXP_PROPERTYSTORAGE_SIG gekennzeichnet sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>Enthält einen zusätzlichen, von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>ishelllinkdatalist</strong></a>verwendeten Datenblock. Sie enthält spezielle Ordner Informationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>Enthält einen zusätzlichen, von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>ishelllinkdatalist</strong></a>verwendeten Datenblock. Sie enthält erweiterbare Umgebungs Zeichenfolgen für das Symbol oder das Ziel.<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>Enthält Informationen über eine Schaltfläche, die von einer Datei-Manager-Erweiterungs-DLL der Symbolleiste des Datei-Managers hinzugefügt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>Extrasearch</strong></a><br/></td>
<td>Wird von einem <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>ienumextrasearch</strong></a> -Enumeratorobjekt verwendet, um Informationen zu den Such Objekten zurückzugeben, die von einem shellordnerobjekt unterstützt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>Enthält die Format Definition der Zwischenablage für CFSTR_FILE_ATTRIBUTES_ARRAY.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>Dateideskriptor</strong></a><br/></td>
<td>Beschreibt die Eigenschaften einer Datei, die während eines Microsoft-ActiveX <a href="dragdrop.md">-Drag & Drop-</a> Vorgangs mithilfe der Zwischenablage kopiert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>Filegroupdescriptor</strong></a><br/></td>
<td>Definiert das CF_FILEGROUPDESCRIPTOR Zwischenablage Format.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>Enthält Informationen über das im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse") ausgewählte Laufwerk.<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse").<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls Element hinzuzufügen<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>Enthält Informationen, die der Datei-Manager zum Hinzufügen eines benutzerdefinierten Menüs verwendet, das von einer Datei-Manager-Erweiterungs-DLL Die Struktur bietet auch einen Delta Wert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>Enthält Informationen über benutzerdefinierte Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden. Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>Foldersettings</strong></a><br/></td>
<td>Enthält Informationen zur Ordner Sicht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>Fvshowinfo</strong></a><br/></td>
<td>Enthält Informationen, die der Datei-Viewer zum Anzeigen einer Datei verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>Enthält Informationen zu einem Element, für das die kontextbezogene Hilfe angefordert wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>Helpwininfo</strong></a><br/></td>
<td>Enthält die Größe und Position eines primären oder sekundären Hilfe Fensters. Eine Anwendung kann diese Informationen durch Aufrufen der <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> -Funktion mit dem HELP_SETWINPOS Wert festlegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>Wird von Microsoft Internet Explorer 4,0 und Microsoft Internet Explorer 4,01 zum Speichern von Informationen zu einer Komponente verwendet. Bei Windows 2000 wird es durch die <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>Komponenten</strong></a> Struktur ersetzt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>Itemittellist</strong></a><br/></td>
<td>Enthält eine Liste der Element Bezeichner.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ItemSpacing</strong></a><br/></td>
<td>Speichert die Dimensionen der zwei möglichen Größen von Symbol Abstände, die für die Anzeige verfügbar sind: klein und groß. Wird von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>ishellfolderview:: getitemspacing</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>Definiert die Besonderheiten eines bekannten Ordners.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>"LogFont"</strong></a><br/></td>
<td>Definiert die Attribute einer Schriftart.<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>Mruinfo</strong></a><br/></td>
<td>Enthält Informationen, die eine neue Liste der zuletzt verwendeten (MRU) definieren. Wird von " <a href="createmrulist.md"><strong>kreatemrulistw</strong></a>" verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>Multikeyhelp</strong></a><br/></td>
<td>Gibt ein Schlüsselwort für die Suche und die Schlüsselwort Tabelle an, die von der Windows-Hilfe gesucht werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a><br/></td>
<td>Enthält Informationen, in denen eine Netzwerkadresse beschrieben wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a><br/></td>
<td>Beschreibt eine Netzwerkadresse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>Newcplinfo</strong></a><br/></td>
<td>Enthält Ressourcen Informationen und einen von der Anwendung definierten Wert für ein Dialogfeld, das von einer System Steuerungsanwendung unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>Notier\data</strong></a><br/></td>
<td>Enthält Informationen, die das System benötigt, um Benachrichtigungen im Benachrichtigungsbereich anzuzeigen. Wird von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>Notisyienidentifier</strong></a><br/></td>
<td>Enthält Informationen, die von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> verwendet werden, um das Symbol zu identifizieren, für das das umgebende Rechteck abgerufen werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>Nresarray</strong></a><br/></td>
<td>Definiert das CF_NETRESOURCE Zwischenablage Format.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>Nstccustomdraw</strong></a><br/></td>
<td>Benutzerdefinierte Zeichnungs Struktur, die von <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>inamespacetreecontrolcustomdraw</strong></a> -Methoden verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>Enthält einen zusätzlichen, von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>ishelllinkdatalist</strong></a>verwendeten Datenblock. Sie enthält Konsolen Eigenschaften.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>Enthält einen zusätzlichen, von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>ishelllinkdatalist</strong></a>verwendeten Datenblock. Sie enthält die Codepage der Konsole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>Identifiziert ein bestimmtes Eigenschaften Blatt in den Eigenschaften Seiten eines Druckers und gibt an, ob dieses Eigenschaften Blatt modal sein soll. Wird optional mit der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>shinvokeprintercommand</strong></a> -Funktion verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>Openasinfo</strong></a><br/></td>
<td>Speichert Informationen für die <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>shopenwithdialog</strong></a> -Funktion.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>Überlappende</strong></a><br/></td>
<td>Enthält Informationen, die in einer asynchronen (überlappenden) Eingabe/Ausgabe (e/a) verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>Paramel</strong></a><br/></td>
<td>Wird von der Funktion " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>Parser-URL</strong></a> " zum Zurückgeben der analysierten URL verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>Gibt den Zielordner und die zugehörigen Attribute einer Ordner Verknüpfung an. Diese Struktur wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3:: getfoldertargetinfo</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: initializeex</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>Previewhandlerframeinfo</strong></a><br/></td>
<td>Zugriffstasten-Tabellenstruktur. Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame:: GetWindowContext</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>Profilinfo</strong></a><br/></td>
<td>Enthält Informationen, die beim Laden oder Entladen eines Benutzerprofils verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>Pubappinfo</strong></a><br/></td>
<td>Bietet Informationen über eine veröffentlichte Anwendung von einem Anwendungs Herausgeber zum <strong>Hinzufügen/Entfernen von Programmen</strong> in der Systemsteuerung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>Qcminfo</strong></a><br/></td>
<td>Enthält Informationen zum Zusammenführen von Menü Elementen in Windows-Explorer-Menüs.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>Qitab</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>qisearch</strong></a> -Funktion verwendet, um eine einzelne Schnittstelle zu beschreiben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>Serializedpropertyvalue</strong></a><br/></td>
<td>Ein Speicherbereich eines beliebigen Typs, der eine serialisierte <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> -Struktur darstellt. Programme sollten den Inhalt eines <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>serializedpropertyvalue</strong></a>nicht überprüfen. Stattdessen sollten Sie Sie mit den Funktionen " <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>stgserializepropvariant</strong></a> " und " <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>stgdeserializepropvariant</strong></a> " bearbeiten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>Diese Struktur wird zusammen mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>shkreateshellfolderview</strong></a> -Funktion verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>Speichert Positionsinformationen für ein Element. Wird mit Message <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>Enthält den Namen einer HTML-Hilfedatei und ein Thema in dieser Datei. Wird mit der <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> Benachrichtigung verwendet. Diese Struktur erfordert Unicode-Zeichen folgen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>Enthält die Details einer Seite, die dem <strong>Eigenschaften</strong> Blatt eines Objekts hinzugefügt werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>Shardappidinfo</strong></a><br/></td>
<td>Enthält Daten, die von " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>shaddtor ecentdocs</strong></a> " verwendet werden, um ein Element zu identifizieren – in diesem Fall als <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>– und den Prozess, dem es zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>Shardappidinfoidlist</strong></a><br/></td>
<td>Enthält Daten, die von " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>shaddtor ecentdocs</strong></a> " verwendet werden, um ein Element zu identifizieren – in diesem Fall durch eine absolute PIDL – und den Prozess, dem es zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>Shardappidinfolink</strong></a><br/></td>
<td>Enthält Daten, die von " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>shaddtor ecentdocs</strong></a> " verwendet werden, um ein Element (in diesem Fall über einen <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>) und den Prozess, dem es zugeordnet ist, zu identifizieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>Shchangenotifyentry</strong></a><br/></td>
<td>Enthält Informationen zu Änderungs Benachrichtigungen und empfängt diese. Diese Struktur wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>shchangenotifyregister</strong></a> -Funktion und der <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> Benachrichtigung verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>Shcolumndata</strong></a><br/></td>
<td>Enthält Informationen, mit denen eine bestimmte Datei identifiziert wird. Sie wird von <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>icolumnprovider:: GetItemData</strong></a> verwendet, wenn Daten für eine bestimmte Datei angefordert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>Shcolumnid</strong></a><br/></td>
<td>Gibt den fmtid-/PID-Bezeichner einer Spalte an, die in der Detailansicht von Windows-Explorer angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Ab Windows Vista wird <a href="/windows/desktop/shell/objects"><strong>shcolumnid</strong></a> als Legacy Formular angesehen und sollte nicht verwendet werden. Verwenden Sie an dieser Stelle die <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> -Struktur.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>Shcolumninfo</strong></a><br/></td>
<td>Enthält Informationen zu den Eigenschaften einer Spalte. Sie wird von <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>icolumnprovider:: GetColumnInfo</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>Shcolumninit</strong></a><br/></td>
<td>Übergibt Initialisierungs Informationen an <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>icolumnprovider:: Initialize</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>Shdescriptionid</strong></a><br/></td>
<td>Empfängt Elementdaten als Reaktion auf einen Aufrufen von " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>shgetdatafrocenterlist</strong></a>".<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>Shdragimage</strong></a><br/></td>
<td>Enthält die Informationen, die zum Erstellen eines Drag-Bilds erforderlich sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>Definiert die Shell-Element Ressource.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>Shelldetails</strong></a><br/></td>
<td>Meldet ausführliche Informationen zu einem Element in einem Shellordner.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>Shellexecuteingefo</strong></a><br/></td>
<td>Enthält Informationen, die von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>Shellflagstate</strong></a><br/></td>
<td>Enthält einen Satz von Flags, die die aktuellen Shelleinstellungen angeben. Diese Struktur wird mit der Funktion " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>shgetsettings</strong></a> " verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>Shellstate</strong></a><br/></td>
<td>Enthält Einstellungen für den Zustand der Shell. Diese Struktur wird mit der Funktion " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>shgetsetsettings</strong></a> " verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>Shfileingefo</strong></a><br/></td>
<td>Enthält Informationen zu einem Datei Objekt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>Shfleopstruct</strong></a><br/></td>
<td>Enthält Informationen, die von der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> -Funktion zum Ausführen von Datei Vorgängen verwendet werden. <br/>
<blockquote>
[!Note]<br />
Ab Windows Vista wird die Verwendung der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> -Schnittstelle für diese Funktion empfohlen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>Shfoldercustomsettings</strong></a><br/></td>
<td>Enthält benutzerdefinierte Ordner Einstellungen. Diese Struktur wird mit der Funktion " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>shgetsetfoldercustomsettings</strong></a> " verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>Shitemid</strong></a><br/></td>
<td>Definiert einen Element Bezeichner.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>Shnamemapping</strong></a><br/></td>
<td>Enthält die alten und neuen Pfadnamen für jede Datei, die von der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> -Funktion verschoben, kopiert oder umbenannt wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>Shqueryrbinfo</strong></a><br/></td>
<td>Enthält die von der Funktion " <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>shqueryrecyclebin</strong></a> " abgerufenen Größen-und Element Anzahl Informationen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>Shstockiconinfo</strong></a><br/></td>
<td>Empfängt Informationen, die zum Abrufen eines Aktien shellsymbols verwendet werden. Diese Struktur wird in einem Aufrufen von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>shgetstockiconinfo</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>Slowappinfo</strong></a><br/></td>
<td>Stellt spezielle Anwendungsinformationen zum <strong>Hinzufügen/Entfernen von Programmen</strong> in der Systemsteuerung bereit. Diese Struktur gilt nicht für veröffentlichte Anwendungen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>Smcshchangenotifystruct</strong></a><br/></td>
<td>Enthält Informationen über die Änderungs Benachrichtigung. Sie wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>ishellmenucallback:: callbacksm</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>Smdata</strong></a><br/></td>
<td>Enthält Informationen aus einem Menüband.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>Sminfo</strong></a><br/></td>
<td>Enthält Informationen zu einem Element aus einem Menüband.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>Software Info</strong></a><br/></td>
<td>Enthält Informationen zu einem Software Update.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a><br/></td>
<td>Speichert Informationen zum Sortieren einer Spalte, die in der Ordneransicht angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strauch</strong></a><br/></td>
<td>Enthält Zeichen folgen, die von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> -Schnittstellen Methoden zurückgegeben werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>Enthält die Parameter für die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2:: CreateViewWindow2</strong></a> -Methode.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>Definiert einen Handler für eine geplante Synchronisierung. Wird mit <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>isyncschedule:: AddItem</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>Beschreibt die Struktur der Konflikt-ID-Informationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>Syncmgrhandlerinfo</strong></a><br/></td>
<td>Stellt Informationen über den Handler für die Verwendung in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>isyncmgrsync:: gethandlerinfo</strong></a> -Methode bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>Syncmgritem</strong></a><br/></td>
<td>Stellt Informationen zu Elementen bereit, die von der <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>isyncmgrenumitems</strong></a> -Schnittstelle aufgelistet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>Syncmgrlogerrorinfo</strong></a><br/></td>
<td>Stellt Fehlerinformationen zur Verwendung in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>isyncmgrsynchronizecallback:: LogError</strong></a> -Methode bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>Syncmgrprogressitem</strong></a><br/></td>
<td>Stellt Statusinformationen während einer Synchronisierung bereit. Diese Struktur wird mit der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>isyncmgrsynchronizecallback::P rogress</strong></a> -Methode verwendet und entspricht einem einzelnen Synchronisierungs Element.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>Tbinfo</strong></a><br/></td>
<td>Wird mit der <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> Benachrichtigung verwendet, um die Anzahl der Schaltflächen anzugeben, die der Symbolleiste hinzugefügt werden sollen, und wie Sie hinzugefügt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>ThumbButton</strong></a><br/></td>
<td>Wird von den Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> -Schnittstelle verwendet, um Schaltflächen zu definieren, die in einer Symbolleiste verwendet werden, die in die Miniaturansicht<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>Wallpaperopt</strong></a><br/></td>
<td>Enthält die Anzeigeoptionen für das Hintergrundbild. Wird mit Membern der <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>iactivedesktop-</strong></a> Schnittstelle verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>Windowdata</strong></a><br/></td>
<td>Speichert Fenster Daten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>Gibt den Kontext einer Miniaturansicht für die Miniaturansicht an. Wird von <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>ithumbnailsettings:: SetContext</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td>Werte, die von <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>ithumbnailcache:: getminiatur</strong></a> zum Angeben von Optionen für die Extraktion und Anzeige des Miniatur Bilds verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>Enthält einen eindeutigen Bezeichner für eine Miniaturansicht im Miniatur Ansichts Cache des Systems.<br/></td>
</tr>
</tbody>
</table>



 

 

 

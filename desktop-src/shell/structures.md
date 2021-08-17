---
description: In diesem Abschnitt werden die Windows Shellstrukturen beschrieben.
title: Shellstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fa046223ba3aa6a6e98d6e74f623aeaad9e85d3a10148bb688eb385c0e7c22fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675803"
---
# <a name="shell-structures"></a>Shellstrukturen

In diesem Abschnitt werden die Windows Shellstrukturen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a><br/></td>
<td>Eine Struktur variabler Größe, die Informationen zu einem Menüdateinamen enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a><br/></td>
<td>Enthält Informationen zu einem Menüelement.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a><br/></td>
<td>Enthält Informationen zu einer Meldung auf der System-Appbar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a><br/></td>
<td>Stellt Anwendungskategorieinformationen zum Hinzufügen/Entfernen von Programmen in Systemsteuerung bereit. Die <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST-Struktur</strong></a> wird verwendet, um eine vollständige Liste der Kategorien für einen Anwendungsherausgeber zu erstellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a><br/></td>
<td>Stellt eine Liste der unterstützten Anwendungskategorien von einem Anwendungsherausgeber zum Hinzufügen/Entfernen von Programmen in Systemsteuerung bereit. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a><br/></td>
<td>Stellt Informationen zu einer veröffentlichten Anwendung für das Hilfsprogramm Software Systemsteuerung bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a><br/></td>
<td>Definiert Informationen, die von <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> verwendet werden, um eine <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations-Schnittstelle</strong></a> für eine bestimmte Dateizuordnung abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a><br/></td>
<td>Enthält Informationen zu einem Ordnerband. Diese Struktur wird mit den <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>Methoden IShellFolderBand::GetBandInfoSFB</strong></a> und <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand::SetBandInfoSFB</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a><br/></td>
<td>Enthält Informationen zu einer Bandwebsite. Diese Struktur wird mit den Methoden <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite::GetBandSiteInfo</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite::SetBandSiteInfo</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a><br/></td>
<td>Enthält geschützte Member der Basisklasse. <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> definiert den Browserzustand und wird mit <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2::GetBaseBrowserData</strong></a> und <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::P utBaseBrowserData</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a><br/></td>
<td>Definiert die Koordinaten der oberen linken und unteren rechten Ecken eines Rahmenrechtecks.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a><br/></td>
<td>Enthält Parameter für die <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder-Funktion</strong></a> und empfängt Informationen über den vom Benutzer ausgewählten Ordner.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>Enthält Kategorieinformationen. Eine Komponentenkategorie ist eine Gruppe logisch verwandter Component Object Model (COM)-Klassen, die einen gemeinsamen Kategoriebezeichner (Common Category Identifier, CATID) gemeinsam nutzen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>Cida</strong></a><br/></td>
<td>Wird mit dem <a href="clipboard.md">CFSTR_SHELLIDLIST</a> Zwischenablageformat verwendet, um den Zeiger auf eine Elementbezeichnerliste (PIDL) eines oder mehrerer Shellnamespaceobjekte zu übertragen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>Definiert Spalteninformationen. Wird von Membern der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager-Schnittstelle</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a><br/></td>
<td>Enthält Informationen, die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> benötigt werden, um einen Kontextmenübefehl aufzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a><br/></td>
<td>Enthält erweiterte Informationen zu einem Kontextmenübefehl. Diese Struktur ist eine erweiterte Version von <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO,</strong></a> die die Verwendung von Unicode-Werten ermöglicht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>Wird generisch zum Filtern von Elementen verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>Komponente</strong></a><br/></td>
<td>Wird von Windows 2000 zum Speichern von Informationen zu einer Komponente verwendet. Diese Struktur ersetzt die <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT-Struktur.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a><br/></td>
<td>Enthält die Desktopelementoptionen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a><br/></td>
<td>Enthält Informationen zur Position und Größe einer Komponente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a><br/></td>
<td>Wird von Windows 2000 verwendet, um Informationen zum Zustand einer Komponente zu speichern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>Definiert die Konfliktelementstruktur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>Definiert die Struktur der Konfliktergebnisinformationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a><br/></td>
<td>Enthält Ressourceninformationen und einen von der Anwendung definierten Wert für ein Dialogfeld, das von einer Systemsteuerung Anwendung unterstützt wird. Die <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet-Funktion</strong></a> der Systemsteuerung Anwendung gibt diese Informationen als Reaktion auf eine CPL_INQUIRE Meldung an <a href="cpl-inquire.md"><strong>den Systemsteuerung</strong></a> zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a><br/></td>
<td>Enthält Details zu Anmeldeinformationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a><br/></td>
<td>Beschreibt ein einzelnes Feld in anmeldeinformationen. Beispielsweise eine Zeichenfolge oder ein Benutzerbild.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a><br/></td>
<td>Wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>Dient als Header für einige der zusätzlichen Datenstrukturen, die von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a><br/></td>
<td>Enthält Kontextmenüinformationen, die von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a><br/></td>
<td>Wird von Delegatordnern anstelle einer <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>STANDARDMÄßIGEN ITEMIDLIST-Struktur</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a><br/></td>
<td>Enthält Detailinformationen für ein Shell-Ordnerelement. Wird mit der <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> Benachrichtigung verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a><br/></td>
<td>Enthält zusätzliche Argumente, die von <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a><br/></td>
<td>Empfängt DLL-spezifische Versionsinformationen. Sie wird mit der <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion-Funktion</strong></a> verwendet. <br/>
<blockquote>
[!Note]<br />
Anstelle dieser Struktur können Sie die <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2-Struktur</strong></a> verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>Empfängt DLL-spezifische Versionsinformationen. Sie wird mit der <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a><br/></td>
<td>Beschreibt das Bild und den zugehörigen Text für ein Drop-Objekt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a><br/></td>
<td>Definiert das <a href="clipboard.md">CF_HDROP</a> Zwischenablageformat. Die folgenden Daten sind eine doppelt auf NULL endende Liste von Dateinamen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>Enthält einen zusätzlichen Datenblock, der von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>verwendet wird. Sie enthält die Windows Installer-ID des Links.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>Speichert Informationen zum Shell-Linkstatus. Diese Struktur wird für zusätzliche Datenabschnitte verwendet, die mit EXP_PROPERTYSTORAGE_SIG gekennzeichnet sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>Enthält einen zusätzlichen Datenblock, der von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>verwendet wird. Sie enthält spezielle Ordnerinformationen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>Enthält einen zusätzlichen Datenblock, der von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>verwendet wird. Sie enthält erweiterbare Umgebungszeichenfolgen für das Symbol oder Ziel.<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>Enthält Informationen zu einer Schaltfläche, die eine Dateierweiterungs-DLL zur Symbolleiste des Datei-Managers hinzufügt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a><br/></td>
<td>Wird von einem <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch-Enumeratorobjekt</strong></a> verwendet, um Informationen zu den Suchobjekten zurückzugeben, die von einem Shellordnerobjekt unterstützt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>Enthält die Zwischenablageformatdefinition für CFSTR_FILE_ATTRIBUTES_ARRAY.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a><br/></td>
<td>Describes the properties of a file that is being copied by means of the clipboard during a Microsoft ActiveX <a href="dragdrop.md">drag-and-drop</a> operation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a><br/></td>
<td>Definiert das format CF_FILEGROUPDESCRIPTOR Zwischenablage.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>Enthält Informationen über das Laufwerk, das im aktiven Datei-Manager-Fenster ausgewählt wurde (das Verzeichnisfenster oder das Fenster Suchergebnisse).<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (das Verzeichnisfenster oder das Fenster Suchergebnisse).<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement hinzuzufügen.<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>Enthält Informationen, die der Datei-Manager verwendet, um ein benutzerdefiniertes Menü hinzuzufügen, das von einer Dateierweiterungs-DLL bereitgestellt wird. Die -Struktur stellt auch einen Deltawert bereit, mit dem die Erweiterungs-DLL das benutzerdefinierte Menü bearbeiten kann, nachdem der Datei-Manager das Menü geladen hat.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Symbolleiste des Datei-Managers hinzugefügt werden sollen. Die Schaltflächen werden von einer Dateierweiterungs-DLL bereitgestellt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a><br/></td>
<td>Enthält Informationen zur Ordneransicht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a><br/></td>
<td>Enthält Informationen, die der Datei-Viewer zum Anzeigen einer Datei verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>Enthält Informationen zu einem Element, für das kontextbezogene Hilfe angefordert wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a><br/></td>
<td>Enthält die Größe und Position eines primären oder sekundären Hilfefensters. Eine Anwendung kann diese Informationen festlegen, indem sie die <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp-Funktion</strong></a> mit dem wert HELP_SETWINPOS aufruft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>Wird von Microsoft Internet Explorer 4.0 und Microsoft Internet Explorer 4.01 verwendet, um Informationen zu einer Komponente zu speichern. Mit Windows 2000 wird sie durch die <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>COMPONENT-Struktur</strong></a> ersetzt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a><br/></td>
<td>Enthält eine Liste von Elementbezeichnern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a><br/></td>
<td>Speichert die Abmessungen der beiden möglichen Symbolabstandsgrößen, die für die Anzeige verfügbar sind: klein und groß. Wird von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView::GetItemSpacing</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>Definiert die Besonderheiten eines bekannten Ordners.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>Logfont</strong></a><br/></td>
<td>Definiert die Attribute einer Schriftart.<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>MRUINFO</strong></a><br/></td>
<td>Enthält Informationen, die eine neue MRU-Liste (Most Recently Used) definieren. Wird von <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a><br/></td>
<td>Gibt ein Schlüsselwort an, nach dem gesucht werden soll, und die Schlüsselworttabelle, die von Windows Hilfe durchsucht werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a><br/></td>
<td>Enthält Informationen, die eine Netzwerkadresse beschreiben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a><br/></td>
<td>Beschreibt eine Netzwerkadresse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a><br/></td>
<td>Enthält Ressourceninformationen und einen von der Anwendung definierten Wert für ein Dialogfeld, das von einer Systemsteuerung Anwendung unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a><br/></td>
<td>Enthält Informationen, die das System benötigt, um Benachrichtigungen im Infobereich anzuzeigen. Wird von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a><br/></td>
<td>Enthält Informationen, die von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> verwendet werden, um das Symbol zu identifizieren, für das das umgebende Rechteck abgerufen werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a><br/></td>
<td>Definiert das CF_NETRESOURCE Zwischenablageformat.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a><br/></td>
<td>Benutzerdefinierte Draw-Struktur, die von <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw-Methoden</strong></a> verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>Enthält einen zusätzlichen Datenblock, der von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>verwendet wird. Sie enthält Konsoleneigenschaften.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>Enthält einen zusätzlichen Datenblock, der von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>verwendet wird. Sie enthält die Codepage der Konsole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>Identifiziert ein bestimmtes Eigenschaftenblatt auf den Eigenschaftenseiten eines Druckers und gibt an, ob dieses Eigenschaftenblatt modal sein soll. Optional mit der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a><br/></td>
<td>Speichert Informationen für die <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog-Funktion.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>Überlappende</strong></a><br/></td>
<td>Enthält Informationen, die in asynchroner (überlappender) Eingabe/Ausgabe (E/A) verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseURL-Funktion</strong></a> verwendet, um die analysierte URL zurückzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>Gibt den Zielordner und die Attribute einer Ordnerverknüpfung an. Diese Struktur wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3::GetFolderTargetInfo</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a><br/></td>
<td>Zugriffstastentabellenstruktur. Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame::GetWindowContext</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>Profileinfo</strong></a><br/></td>
<td>Enthält Informationen, die beim Laden oder Entladen eines Benutzerprofils verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a><br/></td>
<td>Stellt Informationen zu einer veröffentlichten Anwendung von einem Anwendungsherausgeber zum <strong>Hinzufügen/Entfernen</strong> von Programmen in Systemsteuerung bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a><br/></td>
<td>Enthält Informationen zum Zusammenführen von Menüelementen in Windows Explorer-Menüs.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch-Funktion</strong></a> verwendet, um eine einzelne Schnittstelle zu beschreiben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a><br/></td>
<td>Ein Speicherbereich eines beliebigen Typs, der eine serialisierte <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT-Struktur</strong></a> darstellt. Programme sollten den Inhalt eines <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>nicht untersuchen. Stattdessen sollten sie es mit den Funktionen <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> und <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> bearbeiten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>Diese Struktur wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>Speichert Positionsinformationen für ein Element. Wird mit der Meldung <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>Enthält den Namen einer HTML-Hilfedatei und eines Themas in dieser Datei. Wird mit der <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> Benachrichtigung verwendet. Diese Struktur erfordert Unicode-Zeichenfolgen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>Enthält die Details einer Seite, die dem <strong>Eigenschaftenblatt</strong> eines Objekts hinzugefügt werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a><br/></td>
<td>Enthält Daten, die von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> verwendet werden, um sowohl ein Element (in diesem Fall als <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem)</strong></a>als auch den Prozess zu identifizieren, dem es zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a><br/></td>
<td>Enthält Daten, die von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> verwendet werden, um sowohl ein Element ( in diesem Fall durch eine absolute PIDL) als auch den Prozess zu identifizieren, dem es zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a><br/></td>
<td>Enthält Daten, die von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> verwendet werden, um sowohl ein Element, in diesem Fall über einen <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink,</strong></a>als auch den Prozess zu identifizieren, dem es zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a><br/></td>
<td>Enthält Informationen zu Änderungsbenachrichtigungen und empfängt diese. Diese Struktur wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister-Funktion</strong></a> und der <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY-Benachrichtigung</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a><br/></td>
<td>Enthält Informationen, die eine bestimmte Datei identifizieren. Sie wird von <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> verwendet, wenn Daten für eine bestimmte Datei angefordert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a><br/></td>
<td>Gibt den FMTID-/PID-Bezeichner einer Spalte an, die von der Detailansicht des Windows Explorers angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Ab Windows Vista gilt <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> als Legacyformular und sollte nicht verwendet werden. Verwenden Sie stattdessen die <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY-Struktur.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a><br/></td>
<td>Enthält Informationen zu den Eigenschaften einer Spalte. Sie wird von <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider::GetColumnInfo</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a><br/></td>
<td>Übergibt Initialisierungsinformationen an <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider::Initialize</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a><br/></td>
<td>Empfängt Elementdaten als Reaktion auf einen Aufruf von <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a><br/></td>
<td>Enthält die Informationen, die zum Erstellen eines Ziehbilds erforderlich sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>Definiert die Shellelementressource.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a><br/></td>
<td>Gibt ausführliche Informationen zu einem Element in einem Shellordner an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a><br/></td>
<td>Enthält Informationen, die von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a><br/></td>
<td>Enthält einen Satz von Flags, die die aktuellen Shelleinstellungen angeben. Diese Struktur wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a><br/></td>
<td>Enthält Einstellungen für den Zustand der Shell. Diese Struktur wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a><br/></td>
<td>Enthält Informationen zu einem Dateiobjekt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a><br/></td>
<td>Enthält Informationen, die die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation-Funktion</strong></a> zum Ausführen von Dateivorgängen verwendet. <br/>
<blockquote>
[!Note]<br />
Ab Windows Vista wird die Verwendung der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation-Schnittstelle</strong></a> für diese Funktion empfohlen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a><br/></td>
<td>Enthält benutzerdefinierte Ordnereinstellungen. Diese Struktur wird mit der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a><br/></td>
<td>Definiert einen Elementbezeichner.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a><br/></td>
<td>Enthält die alten und neuen Pfadnamen für jede Datei, die von der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation-Funktion</strong></a> verschoben, kopiert oder umbenannt wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a><br/></td>
<td>Enthält die Größen- und Elementanzahlinformationen, die von der <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin-Funktion</strong></a> abgerufen werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a><br/></td>
<td>Empfängt Informationen, die zum Abrufen eines Stock Shell-Symbols verwendet werden. Diese Struktur wird in einem Aufruf <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>von SHGetStockIconInfo</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a><br/></td>
<td>Stellt spezielle Anwendungsinformationen zum <strong>Hinzufügen/Entfernen von Programmen</strong> in Systemsteuerung bereit. Diese Struktur gilt nicht für veröffentlichte Anwendungen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a><br/></td>
<td>Enthält Informationen zur Änderungsbenachrichtigung. Sie wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback::CallbackSM</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a><br/></td>
<td>Enthält Informationen aus einem Menüband.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a><br/></td>
<td>Enthält Informationen zu einem Element aus einem Menüband.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a><br/></td>
<td>Enthält Informationen zu einem Softwareupdate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a><br/></td>
<td>Speichert Informationen zum Sortieren einer Spalte, die in der Ordneransicht angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a><br/></td>
<td>Enthält Zeichenfolgen, die von den <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder-Schnittstellenmethoden</strong></a> zurückgegeben werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>Enthält die Parameter für die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2::CreateViewWindow2-Methode.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>Definiert einen Handler für eine geplante Synchronisierung. Wird mit <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule::AddItem</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>Beschreibt die Konflikt-ID-Informationsstruktur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a><br/></td>
<td>Stellt Informationen zum Handler für die Verwendung in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize::GetHandlerInfo-Methode</strong></a> bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMBUTTEM</strong></a><br/></td>
<td>Stellt Informationen zu Elementen bereit, die von der <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems-Schnittstelle</strong></a> aufzählt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a><br/></td>
<td>Stellt Fehlerinformationen für die Verwendung in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback::LogError-Methode</strong></a> bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a><br/></td>
<td>Stellt Statusinformationen bereit, während eine Synchronisierung ausgeführt wird. Diese Struktur wird mit der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback::P rogress-Methode</strong></a> verwendet und entspricht einem einzelnen Synchronisierungselement.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a><br/></td>
<td>Wird mit der <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> verwendet, um die Anzahl der Schaltflächen anzugeben, die der Symbolleiste hinzugefügt werden sollen, und wie sie hinzugefügt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a><br/></td>
<td>Wird von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3-Schnittstelle verwendet,</strong></a> um Schaltflächen zu definieren, die in einer Symbolleiste verwendet werden, die in die Miniaturansichtsdarstellung eines Fensters eingebettet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a><br/></td>
<td>Enthält die Anzeigeoptionen für das Hintergrundbild. Wird mit Membern der <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop-Schnittstelle</strong></a> verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a><br/></td>
<td>Speichert Fensterdaten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>Gibt den Kontext einer Miniaturansichtsextraktion an. Wird von <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings::SetContext verwendet.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td>Werte, die <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>von IThumbnailCache::GetThumbnail</strong></a> verwendet werden, um Optionen für die Extraktion und Anzeige des Miniaturbilds anzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>Enthält einen eindeutigen Bezeichner für eine Miniaturansicht im Cache der Systemminiaturansicht.<br/></td>
</tr>
</tbody>
</table>



 

 

 

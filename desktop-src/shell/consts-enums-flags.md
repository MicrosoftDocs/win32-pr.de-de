---
description: In diesem Abschnitt werden die Windows-shellkonstanten, Enumerationen und Flags beschrieben.
title: Shellkonstanten, Enumerationen und Flags
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 638beaa7-a065-4ab3-8eb5-286a306a8f24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2070ef1acc37262a526186862f46afa002c47343
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218905"
---
# <a name="shell-constants-enumerations-and-flags"></a>Shellkonstanten, Enumerationen und Flags

In diesem Abschnitt werden die Windows-shellkonstanten, Enumerationen und Flags beschrieben.

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
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svgio"><strong>_SVGIO</strong></a><br/></td>
<td>Wird mit den Methoden <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items"><strong>ifolderview:: Items</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount"><strong>ifolderview:: ItemCount</strong></a>und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject"><strong>ishellview:: getitemuject</strong></a> verwendet, um die Elemente in ihren Auflistungen einzuschränken oder zu steuern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svsif"><strong>_SVSIF</strong></a><br/></td>
<td>Gibt Flags an, die von <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>ifolderview</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ishellview</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> verwendet werden, um eine anzuwendende Art von Auswahl anzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appactionflags"><strong>Appaktionflags</strong></a><br/></td>
<td>Gibt Anwendungs Verwaltungs Aktionen an, die von einem Anwendungs Verleger unterstützt werden. Diese Flags sind Bitmasken, die an <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getpossibleactions"><strong>ishellapp:: getpossibleactions</strong></a>übergeben werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appinfodataflags"><strong>Appinfodataflags</strong></a><br/></td>
<td>Gibt Anwendungsinformationen an, die von <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getappinfo"><strong>ishellapp:: getappinfo</strong></a>zurückgegeben werden sollen. Diese Flags sind <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>Bitmasken</strong></a> , die im dwMask-Member der <strong>appinfodata</strong> -Struktur verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_orientation"><strong>APPLICATION_VIEW_ORIENTATION</strong></a><br/></td>
<td>Definiert den Satz von Anzeige Orientierungs Modi für ein Fenster (App-Ansicht). Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: getapplicationvieworientation</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: abtapplicationvieworientation</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_size_preference"><strong>APPLICATION_VIEW_SIZE_PREFERENCE</strong></a><br/></td>
<td>Definiert den Satz möglicher Größen Einstellungen für allgemeine Fenster (App-Ansicht). Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference"><strong>ilaunchsourceviewsizepreference:: getsourceviewsizepreference</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference"><strong>ilaunchtargetviewsizepreference:: gettargetviewsizepreference</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state"><strong>APPLICATION_VIEW_STATE</strong></a><br/></td>
<td>Gibt den aktuellen Ansichts Zustand einer Windows Store-App an. Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>iapplicationdesignmodesettings:: setapplicationviewstate</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>iapplicationdesignmodesettings:: isapplicationviewstaatupportiert</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocdata"><strong>Assocdata</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata"><strong>iqueryassociations:: GetData</strong></a> verwendet, um den Typ der Daten zu definieren, die zurückgegeben werden sollen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/shell/assocf_str"><strong>Assocf</strong></a><br/></td>
<td>Stellt Informationen für die <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>iqueryassociations</strong></a> -Schnittstellen Methoden bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>Associationlevel</strong></a><br/></td>
<td>Gibt die Quelle der Standard Zuordnung für eine Dateinamenerweiterung an. Wird von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>iapplicationassociationregistration</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>ASSOCIATIONTYPE</strong></a><br/></td>
<td>Gibt den Typ der Zuordnung für eine Anwendung an. Wird von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>iapplicationassociationregistration</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assockey"><strong>Assockey</strong></a><br/></td>
<td>Gibt den Typ des Schlüssels an, der von <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey"><strong>iqueryassociations:: GetKey</strong></a>zurückgegeben werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr"><strong>Assocstr</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring"><strong>iqueryassociations:: GetString</strong></a> verwendet, um den Typ der Zeichenfolge zu definieren, die zurückgegeben werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action"><strong>ATTACHMENT_ACTION</strong></a><br/></td>
<td>Stellt einen Satz von Flags bereit, die mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute verwendet werden sollen::P rompt</strong></a> , um die Aktion anzugeben, die bei der Benutzer Bestätigung ausgeführt werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt"><strong>ATTACHMENT_PROMPT</strong></a><br/></td>
<td>Stellt einen Satz von Flags bereit, die mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute verwendet werden sollen::P rompt</strong></a> , um den Typ der anzuzeigenden Benutzeroberfläche anzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-autocompletelistoptions"><strong>Autocompletelistoptions</strong></a><br/></td>
<td>Gibt an, welche Objekte für automatische Vervollständigungs Listen aufgelistet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shldisp/ne-shldisp-autocompleteoptions"><strong>Autocompleteoptions</strong></a><br/></td>
<td>Gibt die Werte an, die von <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-getoptions"><strong>IAutoComplete2:: GetOptions</strong></a> und <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions"><strong>IAutoComplete2:: abtions</strong></a> für Optionen im Zusammenhang mit AutoComplete verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="str-constants.md"><strong>Binden von Kontext Zeichen folgen Schlüsseln</strong></a><br/></td>
<td>Ein Satz von Zeichen folgen Schlüsseln, die mit der <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> -Methode verwendet werden, um einen Bindungs Kontext anzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shdeprecated/ne-shdeprecated-bnstate"><strong>Bnstate</strong></a><br/></td>
<td>Veraltet. Wird von <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate"><strong>ibrowserservice:: setnavigatestate</strong></a> und <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate"><strong>ibrowserservice:: getnavigatestate</strong></a> zum Angeben von Navigations Zuständen verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-_browserframeoptions"><strong>Browserframeoptions</strong></a><br/></td>
<td>Wird mit der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions"><strong>ibrowserframeoptions:: getframeoptions</strong></a>-Methode verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags"><strong>CATEGORYINFO_FLAGS</strong></a><br/></td>
<td>Stellt einen Satz von Flags für die Verwendung mit der <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a> -Struktur bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags"><strong>CATSORT_FLAGS</strong></a><br/></td>
<td>Gibt Methoden zum Sortieren von Kategoriedaten an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)"><strong>Cdcontrolstate</strong></a><br/></td>
<td>Gibt die Werte an, die angeben, ob ein Steuerelement sichtbar und aktiviert ist. Wird von Membern der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags"><strong>CM_ENUM_FLAGS</strong></a><br/></td>
<td>Wird von Membern der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> -Schnittstelle verwendet, um anzugeben, welche Gruppe von Spalten angefordert werden, entweder alle oder nur die aktuell sichtbaren Spalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask"><strong>CM_MASK</strong></a><br/></td>
<td>Gibt an, welche Werte in der <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> Struktur bei Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo"><strong>icolumnmanager:: setcolumninfo</strong></a>festgelegt werden sollen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value"><strong>CM_SET_WIDTH_VALUE</strong></a><br/></td>
<td>Gibt die Breitenwerte in Pixel an und bietet spezielle Unterstützung für Standard und AutoSize. Wird von Membern der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> -Schnittstelle über die <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> -Struktur verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state"><strong>CM_STATE</strong></a><br/></td>
<td>Gibt Spalten Zustands Werte an. Wird von Membern der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> -Schnittstelle über die <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> -Struktur verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_account_options"><strong>CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS</strong></a><br/></td>
<td>Gibt den Typ der Anmelde Informationen an, die ein Anmelde Informationsanbieter zurückgeben soll, um der &quot; anderen Benutzer &quot; Kachel zuzuordnen. Wird von <a href="/windows/desktop/api/CredentialProvider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions"><strong>ICredentialProviderUserArray_GetAccountOptions</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_credential_field_options"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</strong></a><br/></td>
<td>Stellt Anpassungsoptionen für ein einzelnes Feld in einer Anmelde-oder Anmelde Informationen-Benutzeroberfläche bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state"><strong>CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</strong></a><br/></td>
<td>Beschreibt den Status eines Felds und die Art und Weise, wie ein Benutzer damit interagieren kann. Felder können von einem Anmelde Informationsanbieter in einer Vielzahl unterschiedlicher interaktiver Zustände angezeigt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_state"><strong>CREDENTIAL_PROVIDER_FIELD_STATE</strong></a><br/></td>
<td>Gibt den Status eines einzelnen Felds in der Benutzeroberfläche für Anmelde Informationen an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_type"><strong>CREDENTIAL_PROVIDER_FIELD_TYPE</strong></a><br/></td>
<td>Gibt einen Typ von Anmelde Informationsfeldern an. Wird von <a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_get_serialization_response"><strong>CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</strong></a><br/></td>
<td>Beschreibt die Antwort, wenn ein Anmelde Informationsanbieter versucht, Anmelde Informationen zu serialisieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_status_icon"><strong>CREDENTIAL_PROVIDER_STATUS_ICON</strong></a><br/></td>
<td>Gibt an, welches Statussymbol angezeigt werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_usage_scenario"><strong>CREDENTIAL_PROVIDER_USAGE_SCENARIO</strong></a><br/></td>
<td>Deklariert die Szenarien, in denen ein Anmelde Informationsanbieter unterstützt wird. Ein Verwendungs Szenario (CPUs) des Anmelde Informationsanbieters ermöglicht es dem Anmelde Informationsanbieter, unterschiedliche enumerationsverhalten und das Einrichten von Benutzeroberflächen Feldern in Szenarios bereitzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="csidl.md"><strong>CSIDL</strong></a><br/></td>
<td><blockquote>
<p><b>Hinweis: </b> Ab Windows Vista wurden diese Werte durch <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> -Werte ersetzt. In diesem Thema finden Sie eine Liste der neuen Konstanten und ihrer entsprechenden CSIDL-Werte. Der benutzerfreundlicher Name werden auch die entsprechenden <strong>KNOWNFOLDERID</strong> -Werte für jeden CSIDL-Wert angegeben.</p>
<p>Das CSIDL-System wird unter Windows Vista aus Kompatibilitätsgründen unterstützt. Die neue Entwicklung sollte jedoch anstelle von CSIDL-Werten <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> -Werte verwenden.<br/></p>
</blockquote>
<br/> CSIDL-Werte (Konstante sonderelement-ID-Liste) stellen eine eindeutige systemunabhängige Methode dar, um spezielle Ordner zu identifizieren, die häufig von Anwendungen verwendet werden, aber nicht denselben Namen oder Speicherort auf einem beliebigen System haben. Der Systemordner kann z &quot; . b. c:\Windows &quot; auf einem System und &quot; c:\WINNT &quot; auf einem anderen System sein. Diese Konstanten werden in "shlobj. h" definiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="ctf.md"><strong>CTF-Flags</strong></a><br/></td>
<td>Flags, die das Verhalten der aufrufenden Funktion steuern. Wird von <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread"><strong>shkreatethread</strong></a> und <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle"><strong>shkreatethlewithhandle</strong></a>verwendet. In diesen Funktionen sind diese Werte so definiert, dass Sie vom Typ SHCT_FLAGS sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags"><strong>DATAOBJ_GET_ITEM_FLAGS</strong></a><br/></td>
<td>Werte, die von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>shgetitemfromdataobject</strong></a> -Funktion zum Angeben von Optionen für die Verarbeitung des Quell Objekts verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-tagdeskbandcid"><strong>DBID-Befehlsflags</strong></a><br/></td>
<td>Diese Befehls-IDs können mit <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec"><strong>IOleCommandTarget:: exec</strong></a>an den Container des Band Objekts gesendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id"><strong>DEF_SHARE_ID</strong></a><br/></td>
<td>Werte, die den Ordner angeben, auf dem durch Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>isharingconfigurationmanager</strong></a> -Schnittstelle gearbeitet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype"><strong>Defaultsavefoldertype</strong></a><br/></td>
<td>Gibt den Standard Speicherort an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-default_folder_menu_restrictions"><strong>DEFAULT_FOLDER_MENU_RESTRICTIONS</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position"><strong>DESKTOP_WALLPAPER_POSITION</strong></a><br/></td>
<td>Gibt an, wie das Hintergrundbild des Desktops angezeigt werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ne-shtypes-device_scale_factor"><strong>DEVICE_SCALE_FACTOR</strong></a><br/></td>
<td>Gibt einen gefälschten Geräte Skalierungsfaktor als Prozentsatz an. Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>iapplicationdesignmodesettings:: setapplicationviewstate</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>iapplicationdesignmodesettings:: isapplicationviewstaatupportiert</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-display_device_type"><strong>DISPLAY_DEVICE_TYPE</strong></a><br/></td>
<td>Gibt an, ob das Gerät eine primäre oder immersive Art von Anzeige ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype"><strong>Dropimagetype</strong></a><br/></td>
<td>Werte, die mit der <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>dropdescription</strong></a> -Struktur zum Angeben des Ablage Bilds verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>Expcmdstate</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>Expcmdstate</strong></a> -Werte stellen den Befehls Zustand eines shellelements dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags"><strong>EXPLORER_BROWSER_FILL_FLAGS</strong></a><br/></td>
<td>Diese Flags werden mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject"><strong>IExplorerBrowser:: fillfromuject</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options"><strong>EXPLORER_BROWSER_OPTIONS</strong></a><br/></td>
<td>Diese Flags werden mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions"><strong>IExplorerBrowser:: GetOptions</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions"><strong>IExplorerBrowser::-toptions</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_explorerpanestate"><strong>Explorerpanestate</strong></a><br/></td>
<td>Kennzeichnen Sie Flags, die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate"><strong>iexplorerpanevisibility:: getpanestate</strong></a> verwendet werden, um den aktuellen Zustand des angegebenen Windows-Explorer-Bereichs zu erhalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap"><strong>"F"</strong></a><br/></td>
<td>Gibt die Platzierung der Liste an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response"><strong>FDE_OVERWRITE_RESPONSE</strong></a><br/></td>
<td>Gibt die Werte an, die von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite"><strong>IFileDialogEvents:: onüberschreibungsmethode</strong></a> zum Angeben der Reaktion einer Anwendung auf eine Überschreibungs Anforderung während eines Speicher Vorgangs mithilfe des allgemeinen Datei Dialogfelds verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response"><strong>FDE_SHAREVIOLATION_RESPONSE</strong></a><br/></td>
<td>Gibt die Werte an, die von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation"><strong>IFileDialogEvents:: onshareverletzungs</strong></a> -Methode verwendet werden, um die Reaktion einer Anwendung auf eine Freigabe Verletzung anzugeben, die auftritt, wenn eine Datei geöffnet oder gespeichert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode"><strong>FFFP_MODE</strong></a><br/></td>
<td>Beschreibt Übereinstimmungs Kriterien. Wird von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>iknownfoldermanager</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type"><strong>FILE_USAGE_TYPE</strong></a><br/></td>
<td>Konstanten, die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage"><strong>ifleisinuse:: getusage</strong></a> verwendet werden, um anzugeben, wie eine verwendete Datei verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions"><strong>Fileopendialogoptions</strong></a><br/></td>
<td>Definiert den Satz von Optionen, der für ein Dialogfeld zum Öffnen oder speichern verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>Filetypeattributeflags</strong></a><br/></td>
<td>Gibt <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>filetypeattributeflags</strong></a> -Konstanten an, die im EditFlags-Wert eines Registrierungsschlüssels für die Datei Zuordnungs <a href="fa-progids.md">ProgID</a> verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode"><strong>iobjectwithfolderenummode:: getMode</strong></a> -Methode und der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode"><strong>iobjectwithfolderenummode:: setmode</strong></a> -Methode verwendet, um die Anzeigemodi für die Ordner abzurufen und festzulegen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags"><strong>FolderFlags</strong></a><br/></td>
<td>Ein Satz von Flags, die Optionen für die Ordneransicht angeben. Die Flags sind unabhängig voneinander und können in beliebiger Kombination verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode"><strong>Folderlogicalviewmode</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode"><strong>ifolderviewsettings:: getviewmode</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode"><strong>isearchfolderitemfactory:: setfolderlogicalviewmode</strong></a> verwendet, um den Ansichtsmodus zu beschreiben.<br/></td>
</tr>
<tr class="odd">
<td><a href="foldertypeid.md"><strong>Foldertypeid</strong></a><br/></td>
<td>Die <a href="foldertypeid.md"><strong>foldertypeid</strong></a> -Werte stellen eine Ansichts Vorlage dar, die auf einen Ordner angewendet wird, in der Regel basierend auf der vorgesehenen Verwendung und dem Inhalt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode"><strong>Folderviewmode</strong></a><br/></td>
<td>Gibt den Typ der Ordner Sicht an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-folderviewoptions"><strong>Folderviewoptions</strong></a><br/></td>
<td>Wird von Methoden der <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>ifolderviewoptions</strong></a> -Schnittstelle zum Aktivieren von Windows Vista-Optionen verwendet, die in Windows 7 und neueren Systemen standardmäßig nicht unterstützt werden, sowie zum Deaktivieren neuer Windows 7-Optionen.<br/></td>
</tr>
<tr class="even">
<td><a href="iactivedesktop-flags.md"><strong>Iactivedesktop-Flags</strong></a><br/></td>
<td>In diesem Abschnitt werden die von <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>iactivedesktop-</strong></a> Schnittstellen Methoden verwendeten Flags beschrieben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-ieshortcutflags"><strong>Ieshortcutflags</strong></a><br/></td>
<td>Gibt an, wie eine Verknüpfung vom Browser behandelt werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category"><strong>KF_CATEGORY</strong></a><br/></td>
<td>Ein Wert, der eine Kategorie darstellt, durch die ein im bekannten Ordnersystem registrierter Ordner klassifiziert werden kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags"><strong>KF_DEFINITION_FLAGS</strong></a><br/></td>
<td>Flags, die bestimmte bekannte Ordner Verhalten angeben. Wird mit der <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a> -Struktur verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags"><strong>KF_REDIRECT_FLAGS</strong></a><br/></td>
<td>Flags, die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect"><strong>iknownfoldermanager:: Redirect</strong></a> verwendet werden, um Details zu einer bekannten Ordner Umleitung anzugeben, z. b. Berechtigungen und den Besitz des umgeleiteten Ordners.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities"><strong>KF_REDIRECTION_CAPABILITIES</strong></a><br/></td>
<td>Flags, die die aktuellen Umleitungs Funktionen eines bekannten Ordners angeben. Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities"><strong>iknownfolder:: getredirectionfunktionen</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag"><strong>KNOWN_FOLDER_FLAG</strong></a><br/></td>
<td>Legen Sie spezielle Abruf Optionen für bekannte Ordner fest. Diese Werte ersetzen <a href="csidl.md"><strong>CSIDL</strong></a> -Werte, die eine parallele Bedeutung haben.<br/></td>
</tr>
<tr class="odd">
<td><a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a><br/></td>
<td>Die <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> -Konstanten stellen GUIDs dar, mit denen Standardordner identifiziert werden, die im System als <a href="known-folders.md">bekannte Ordner</a>registriert sind. Diese Ordner werden mit Windows Vista und höheren Betriebssystemen installiert, und auf einem Computer sind nur geeignete Ordner installiert. Beschreibungen dieser Ordner finden Sie unter <a href="csidl.md"><strong>CSIDL</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter"><strong>Libraryfolderfilter</strong></a><br/></td>
<td>Definiert Optionen zum Filtern von Ordner Elementen. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions"><strong>Librarymanagedialogoptions</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui"><strong>shshowmanagelibraryui</strong></a> verwendet, um Optionen für die Behandlung eines Namens Konflikts beim Speichern einer Bibliothek zu definieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags"><strong>Libraryoptionflags</strong></a><br/></td>
<td>Gibt die Bibliotheks Optionen an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags"><strong>Librarysaveflags</strong></a><br/></td>
<td>Gibt die Optionen für die Behandlung eines Namens Konflikts beim Speichern einer Bibliothek an. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-mimeassociationdialog_in_flags"><strong>MIMEASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Wird mit der <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>mimeassociationdialog</strong></a> -Funktion verwendet, um zu bestimmen, wie Sie ausgeführt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility"><strong>MONITOR_APP_VISIBILITY</strong></a><br/></td>
<td>Gibt an, ob eine Anzeige Desktop Fenster anstelle von Windows Store-Apps anzeigt.<br/></td>
</tr>
<tr class="even">
<td><a href="mp-popupflags.md"><strong>MP_POPUPFLAGS Konstanten</strong></a><br/></td>
<td>Stellt Optionen dar, die beim Anzeigen eines Popup Menüs verfügbar sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="net-string.md"><strong>NET_STRING</strong></a><br/></td>
<td>Stellen Sie Netzwerk Adresstypen dar. Verwenden Sie mindestens eine (als bitweise Kombination) der folgenden Konstanten, um eine Netzwerk Adress Maske zu erstellen, die mit dem Makro <a href="/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype"><strong>NetAddr_SetAllowType</strong></a>verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nstcfoldercapabilities"><strong>Nstcfolderfunktionen</strong></a><br/></td>
<td>Gibt den Zustand eines Strukturelements an. Diese Werte werden von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>inamespacetreecontrolfolderfunktionalitäten</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate"><strong>Nstcitemstate</strong></a><br/></td>
<td>Gibt den Zustand eines Strukturelements an. Diese Werte werden von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>inamespacetreecontrol</strong></a> -Schnittstelle verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcstyle"><strong>Nstcstyle</strong></a><br/></td>
<td>Beschreibt die Merkmale eines angegebenen Namespace Struktur-Steuer Elements.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-nstcstyle2"><strong>NSTCSTYLE2</strong></a><br/></td>
<td>Wird von den Methoden des <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a> verwendet, um erweiterte Anzeige Stile in der TreeView eines shellnamespaces anzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf"><strong>Nwmf</strong></a><br/></td>
<td>Flags, die von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow"><strong>INewWindowManager:: evaluatenewwindow</strong></a>verwendet werden. Diese Werte sind Faktoren bei der Entscheidung, ob ein Popup Fenster angezeigt werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state"><strong>PACKAGE_EXECUTION_STATE</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-perceived"><strong>Wahr</strong></a><br/></td>
<td>Gibt den wahrgenommenen Typ einer Datei an. Diese Gruppe von Konstanten wird in der Funktion " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype"><strong>assocgetwahrnehmvedtype</strong></a> " verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags"><strong>Pubappinfoflags</strong></a><br/></td>
<td>Gibt an, welche Elemente in der <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>pubappinfo</strong></a> -Struktur gültig sind. Diese Flags sind Bitmasken, die im <strong>dwMask</strong> -Member festgelegt und an <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo"><strong>ipublishedapp:: getpublishedappinfo</strong></a>übergeben werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-query_user_notification_state"><strong>QUERY_USER_NOTIFICATION_STATE</strong></a><br/></td>
<td>Gibt den Zustand des Computers für den aktuellen Benutzer in Bezug auf die Angemessenheit des Sendens einer Benachrichtigung an. Wird von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>shqueryusernotificationstate</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="hkey-type.md"><strong>Registrierungs Datentypen</strong></a><br/></td>
<td>Diese Datentypen können verwendet werden, um den Typ eines Registrierungs Werts anzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="regsam.md"><strong>Regsam</strong></a><br/></td>
<td>Ein Datentyp, der zum Angeben der Sicherheits Zugriffs Attribute in der Registrierung verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions"><strong>Begrenzungen</strong></a><br/></td>
<td>Diese Flags werden mit der Funktion " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>shrestricted</strong></a> " verwendet. Mithilfe von " <strong>shrestricted</strong> " wird ermittelt, ob eine angegebene Administrator Richtlinie wirksam ist. In vielen Fällen müssen Anwendungen bestimmte Verhaltensweisen ändern, um die Richtlinien zu erfüllen, die von Systemadministratoren erlassen werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-scale_change_flags"><strong>SCALE_CHANGE_FLAGS</strong></a><br/></td>
<td>Flags, die verwendet werden, um die aufgetretene Skalierungs Änderung anzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status"><strong>SCNRT_STATUS</strong></a><br/></td>
<td>Gibt an, ob das asynchrone registrieren und Aufheben der Registrierung für <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>shchangenotifyregisterthread</strong></a>aktiviert oder deaktiviert werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-tagsfbs_flags"><strong>SFBS_FLAGS</strong></a><br/></td>
<td>Gibt an, wie die Funktion " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>strautesizeex</strong></a> " die Rundung nicht angezeigter Ziffern behandeln soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="sfgao.md"><strong>Sfgao</strong></a><br/></td>
<td>Attribute, die für ein Element (Datei oder Ordner) oder eine Gruppe von Elementen abgerufen werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shard"><strong>SHARD</strong></a><br/></td>
<td>Gibt die Interpretation der Daten an, die von " <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> " in seinem <em>PV</em> -Parameter übergeben werden, um das Element zu identifizieren, dessen Verwendungs Statistiken nachverfolgt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role"><strong>SHARE_ROLE</strong></a><br/></td>
<td>Gibt die Zugriffsberechtigungen an, die den <strong>Benutzern</strong> oder dem <strong>öffentlichen</strong> Ordner zugewiesen sind. Wird in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare"><strong>den</strong></a> Berechtigungen "" und " <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions"><strong>getshare"</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-shcolstate"><strong>Shcolstate</strong></a><br/></td>
<td>Beschreibt, wie eine Eigenschaft behandelt werden soll. Diese Werte werden in "shtypes. h" definiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shcontf"><strong>Shcontf</strong></a><br/></td>
<td>Bestimmt die Typen von Elementen, die in einer Enumeration enthalten sind. Diese Werte werden mit der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: erumubjects</strong></a> -Methode verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags"><strong>SHELL_LINK_DATA_FLAGS</strong></a><br/></td>
<td>Gibt Options Einstellungen an. Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags"><strong>ishelllinkdatalist:: GetFlags</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-setflags"><strong>ishelllinkdatalist:: setFlags</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a><br/></td>
<td>Identifiziert den Typ der Benutzeroberflächen Komponente, die in der Shell erforderlich ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions"><strong>Shellfolderviewoptions</strong></a><br/></td>
<td>Gibt die von der <a href="shellfolderview-viewoptions.md"><strong>viewoptions</strong></a> -Eigenschaft zurückgegebenen Ansichtsoptionen an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants"><strong>Shellspecialfolderkonstanten</strong></a><br/></td>
<td>Gibt eindeutige, systemunabhängige Werte an, durch die spezielle Ordner identifiziert werden. Diese Ordner werden häufig von Anwendungen verwendet, die jedoch nicht denselben Namen oder Speicherort auf einem beliebigen System haben. Der Systemordner kann z &quot; . b. c:\Windows &quot; auf einem System und &quot; c:\WINNT &quot; auf einem anderen System sein.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ExDisp/ne-exdisp-shellwindowfindwindowoptions"><strong>Shellwindowfindwindowoptions</strong></a><br/></td>
<td>Gibt Optionen für die Suche nach Fenstern in der Windows-Auflistung der Shell an. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/ne-exdisp-shellwindowtypeconstants"><strong>Shellwindowtypekonstanten</strong></a><br/></td>
<td>Gibt die Typen von shellfenstern an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shgdnf"><strong>Shgdnf</strong></a><br/></td>
<td>Definiert die Werte, die mit den Methoden <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof"><strong>IShellFolder:: setnameof</strong></a> verwendet werden, um den Typ der Datei-oder Ordnernamen anzugeben, die von diesen Methoden verwendet werden. <br/>
<blockquote>
<b>Hinweis:</b><br />
Vor Windows 7 wurden diese Werte als shgno-Enumeration verpackt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shglobalcounter"><strong>Shglobalcounter</strong></a><br/></td>
<td>Bezeichner für verschiedene globale Zähler oder freigegebene Variablen. Jeder globale Indikator kann mit " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement"><strong>shglobalcounterincrement</strong></a> " und " <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement"><strong>shglobalcounterdecrement</strong></a>" inkrementiert oder dekrementiert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregdel_flags"><strong>SHREGDEL_FLAGS</strong></a><br/></td>
<td>Stellt einen Satz von Werten bereit, die angeben, aus welchem Basis Schlüssel ein Element gelöscht wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregenum_flags"><strong>SHREGENUM_FLAGS</strong></a><br/></td>
<td>Stellt einen Satz von Werten bereit, die den Basis Schlüssel angeben, der für eine Enumeration verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-shstockiconid"><strong>Shstockiconid</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>shgetstockiconinfo</strong></a> verwendet, um das abzurufende aktiensystem Symbol zu identifizieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_sichintf"><strong>Sichintf</strong></a><br/></td>
<td>Wird verwendet, um zu bestimmen, wie zwei shellelemente verglichen werden sollen. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-compare"><strong>IShellItem:: Compare</strong></a> verwendet diesen enumerierten Typ.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn"><strong>Sigdn</strong></a><br/></td>
<td>Fordert das Abrufen der Form des anzeigen Amens eines Elements über <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname"><strong>IShellItem:: GetDisplayName</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>shgetnamefroferlist</strong></a>an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction"><strong>Spaction</strong></a><br/></td>
<td>Beschreibt eine Aktion, die ausgeführt wird, die dem Benutzer den Status mithilfe einer <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IAction Progress</strong></a> -Schnittstelle angezeigt werden muss.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_spbeginf"><strong>Spbeginf</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin"><strong>iaktionprogress:: begin</strong></a>verwendet, geben diese Konstanten bestimmte UI-Vorgänge an, die aktiviert oder deaktiviert werden sollen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext"><strong>Sptext</strong></a><br/></td>
<td>Gibt den Typ des beschreibenden Texts an, der für eine <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>iaktionprogress</strong></a> -Schnittstelle bereitgestellt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="srrf.md"><strong>Srrf</strong></a><br/></td>
<td>Flags, die die festzulegenden oder zurück zugegenden Daten einschränken.<br/></td>
</tr>
<tr class="odd">
<td><a href="ssf-constants.md"><strong>SSF-Konstanten</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>shgetsetsettings</strong></a> -Funktion verwendet, um anzugeben, welche Member der <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>shellstate</strong></a> -Struktur festgelegt oder abgerufen werden sollen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag"><strong>Stpflag</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties"><strong>ITaskbarList4:: settabproperties</strong></a> -Methode zum Angeben von Registerkarten Eigenschaften verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status"><strong>SVUIA_STATUS</strong></a><br/></td>
<td>Wird mit der <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview"><strong>IBrowserService2:: _UIActivateView</strong></a> -Methode verwendet, um den Zustand einer Browseransicht festzulegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_cancel_request"><strong>SYNCMGR_CANCEL_REQUEST</strong></a><br/></td>
<td>Beschreibt eine Anforderung des Benutzers, eine Synchronisierung abzubrechen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_conflict_item_type"><strong>SYNCMGR_CONFLICT_ITEM_TYPE</strong></a><br/></td>
<td>Beschreibt den Konflikt Elementtyp.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_control_flags"><strong>SYNCMGR_CONTROL_FLAGS</strong></a><br/></td>
<td>Gibt an, wie ein für bestimmte Methoden von <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>isyncmgrcontrol</strong></a> angeforderter Vorgang ausgeführt werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_flags"><strong>SYNCMGR_EVENT_FLAGS</strong></a><br/></td>
<td>Gibt Flags für ein Synchronisierungs Ereignis an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_level"><strong>SYNCMGR_EVENT_LEVEL</strong></a><br/></td>
<td>Gibt den Typ des Ereignisses an, das Sync Center gemeldet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_capabilities"><strong>SYNCMGR_HANDLER_CAPABILITIES</strong></a><br/></td>
<td>Gibt die Funktionen eines Handlers in Bezug auf die Aktionen an, die für ihn ausgeführt werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_policies"><strong>SYNCMGR_HANDLER_POLICIES</strong></a><br/></td>
<td>Listet von einem Synchronisierungs Handler angegebene Richtlinien auf, die von der Standard Richtlinie abweichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_type"><strong>SYNCMGR_HANDLER_TYPE</strong></a><br/></td>
<td>Gibt den Typ eines Handlers an. Wird von <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype"><strong>isyncmgrhandlerinfo:: GetType</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_capabilities"><strong>SYNCMGR_ITEM_CAPABILITIES</strong></a><br/></td>
<td>Gibt die Aktionen an, die für ein Element ausgeführt werden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_policies"><strong>SYNCMGR_ITEM_POLICIES</strong></a><br/></td>
<td>Gibt die Richtlinien eines Elements an, um zu steuern, wie Sie durch die Gruppenrichtlinie aktiviert oder deaktiviert werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_choice"><strong>SYNCMGR_PRESENTER_CHOICE</strong></a><br/></td>
<td>Beschreibt die Auswahl, die ein Benutzer über die Konfliktlösung eines Synchronisierungs-Managers trifft. Wird von <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>isyncmgrconflictpresenter</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_next_step"><strong>SYNCMGR_PRESENTER_NEXT_STEP</strong></a><br/></td>
<td>Beschreibt den nächsten Schritt, der in der Konfliktlösung des Synchronisierungs-Managers ausgeführt werden soll. Wird von <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>isyncmgrconflictpresenter</strong></a>verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_progress_status"><strong>SYNCMGR_PROGRESS_STATUS</strong></a><br/></td>
<td>Gibt den aktuellen Status Status eines Synchronisierungs Vorgangs an. Wird von <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress"><strong>isyncmgrsynccallback:: Report Progress</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_abilities"><strong>SYNCMGR_RESOLUTION_ABILITIES</strong></a><br/></td>
<td>Gibt die Funktionen und die zu befolgenden Konflikt Auflösungs Aktivitäten an. Wird mit <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities"><strong>isyncmgrresolutionhandler:: queryabiliverwendet</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_feedback"><strong>SYNCMGR_RESOLUTION_FEEDBACK</strong></a><br/></td>
<td>Beschreibt Synchronisierungs-Manager Lösungs Feedback. Wird von <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>isyncmgrresolutionhandler</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_sync_control_flags"><strong>SYNCMGR_SYNC_CONTROL_FLAGS</strong></a><br/></td>
<td>Gibt Flags an, die von <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>isyncmgrcontrol:: starthandlersync</strong></a> und <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>isyncmgrcontrol:: startitemsync</strong></a>verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>Syncmgrflag</strong></a><br/></td>
<td>Die <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>syncmgrflag</strong></a> -Enumerationswerte werden in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize"><strong>isyncmgrsync:: Initialize</strong></a> -Methode verwendet, um anzugeben, wie das Synchronisierungs Ereignis initiiert wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrhandlerflags"><strong>Syncmgrhandlerflags</strong></a><br/></td>
<td>Wird in der <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>syncmgrhandlerinfo</strong></a> -Struktur als Flags verwendet, die für den aktuellen Handler gelten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>Syncmgrinvokeflags</strong></a><br/></td>
<td>Der <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>syncmgrinvokeflags</strong></a> -Enumerationswert gibt an, wie der Synchronisierungs-Manager in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems"><strong>isyncmgrsynchronizone voke:: UpdateItems</strong></a> -Methode aufgerufen werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgritemflags"><strong>Syncmgritemflags</strong></a><br/></td>
<td>Gibt Informationen für das aktuelle Element in der <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>syncmgritem</strong></a> -Struktur an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>Syncmgrloglevel</strong></a><br/></td>
<td>Die <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>syncmgrloglevel</strong></a> -Enumerationswerte geben eine Fehler Ebene für die Verwendung in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>isyncmgrsynchronizecallback:: LogError</strong></a> -Methode an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>Syncmgrregisterflags</strong></a><br/></td>
<td>Die <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>syncmgrregisterflags</strong></a> -Enumerationswerte werden in Methoden der <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>isyncmgrregister</strong></a> -Schnittstelle verwendet, um Ereignisse zu identifizieren, für die der Handler für die Benachrichtigung registriert ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrstatus"><strong>Syncmgrstatus</strong></a><br/></td>
<td>Wird in der <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus"><strong>isyncmgrsync:: SetItemStatus</strong></a> -Methode verwendet, um den aktualisierten Status für das Element anzugeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags"><strong>Thumbbuttonflags</strong></a><br/></td>
<td>Wird von <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong></strong></a> der fingerschaltfläche verwendet, um bestimmte Zustände und Verhalten der Schaltfläche zu steuern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask"><strong>Thumbbuttonmask</strong></a><br/></td>
<td>Wird von der <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>ThumbButton</strong></a> -Struktur verwendet, um anzugeben, welche Member dieser Struktur gültige Daten enthalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/ne-thumbnailstreamcache-thumbnailstreamcacheoptions"><strong>Thumbnailstreamcacheoptions</strong></a><br/></td>
<td>Definiert die Cache Optionen, die von der <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>ithumbnailstreamcache</strong></a> -Schnittstelle verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags"><strong>TRANSFER_SOURCE_FLAGS</strong></a><br/></td>
<td>Wird von Methoden der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>itransfersource</strong></a> -Schnittstelle und der <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>itransferdestination</strong></a> -Schnittstelle verwendet, um Ihre Datei Vorgänge zu steuern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a> Enumerationswerte werden mit der <a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>translateurl</strong></a> -Funktion verwendet, um zu bestimmen, wie Sie ausgeführt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-undock_reason"><strong>UNDOCK_REASON</strong></a><br/></td>
<td>Werte, die den Grund angeben, warum ein angedocktes Barrierefreiheits-App-Fenster nicht angedockt wurde. Wird von <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked"><strong>iaccessibilitydockingservicecallback:: nicht angedockt</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-url_scheme"><strong>URL_SCHEME</strong></a><br/></td>
<td>Wird zum Angeben von URL-Schemas verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a> Enumerationswerte werden mit <a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>urlassociationdialog</strong></a> verwendet, um zu bestimmen, wie Sie ausgeführt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpcolorflags"><strong>Vpcolorflags</strong></a><br/></td>
<td>Gibt die Verwendung einer Farbe an. Wird von <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>ivisualproperties</strong></a> -Methoden verwendet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpwatermarkflags"><strong>Vpwatermarkflags</strong></a><br/></td>
<td>Gibt Wasserzeichen Flags an. Wird von <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ivisualproperties-setwatermark"><strong>ivisualproperties:: setwatermark</strong></a>verwendet.<br/></td>
</tr>
</tbody>
</table>



 

 

 

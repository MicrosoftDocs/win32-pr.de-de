---
description: 'Ein Satz von Zeichen folgen Schlüsseln, die mit der IBindCtx:: RegisterObjectParam-Methode verwendet werden, um einen Bindungs Kontext anzugeben.'
title: Binden von Kontext Zeichenfolgen-Schlüsseln (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1dcdb3b9199fede88d6f13949cc9276bde17b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980920"
---
# <a name="bind-context-string-keys"></a>Binden von Kontext Zeichen folgen Schlüsseln

Ein Satz von Zeichen folgen Schlüsseln, die mit der [**IBindCtx:: RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) -Methode verwendet werden, um einen Bindungs Kontext anzugeben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP SP2</strong>. Legen Sie diesen Bindungs Kontext fest, um zuzulassen, dass Clients der Datenquelle die Richtlinie für ausgeblendete Laufwerksbuchstaben überschreiben und den Zugriff auf die Ansichts Objekte für Datenquellen auf den gesperrten Laufwerken aktivieren.<br/> Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> oder <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: bindtohandler</strong></a>verwendet.<br/> Das System unterstützt vom Administrator gesteuerte Richtlinien, die angegebene Laufwerk Buchstaben ausblenden, um Benutzern den Zugriff auf diese Laufwerke über Windows-Explorer zu blockieren. Wenn diese Richtlinie aktiv ist, ist das Ergebnis, dass Ansichts Objekte und andere Handler, die mit der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder::</strong></a> up-Methode erstellt wurden, fehlschlagen, wenn Sie auf Laufwerken aufgerufen werden, die von der-Richtlinie blockiert werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, damit die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindteobject</strong></a> -Methode das vom <em>PBC</em> -Parameter angegebene Objekt verwendet, um das Zielobjekt zu erstellen. in diesem Fall muss das Objekt, das durch den <em>Punk</em> -Parameter im <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> -Befehl angegeben wird, die <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ikreateobject</strong></a> -Schnittstelle implementieren. <br/> Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> oder <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: bindtohandler</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. An <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsec Display Name</strong></a> mit einem <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> Wert, um den enumerationsmodus des analysierten Elements zu steuern. Der <strong>FOLDER_ENUM_MODE</strong> Wert wird im Bindungs Kontext durch ein Objekt, das <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>iobjectwithfolderenummode</strong></a>implementiert, übermittelt. <br/> Elemente mit unterschiedlichen enumerationsmodi vergleichen kanonisch (SHCIDS_CANONICALONLY), da Sie unterschiedliche Sätze von Elementen aufzählen.<br/> Wenn ein Element den enumerationsmodus nicht unterstützt (da es sich nicht um einen Ordner handelt oder der enumerationsmodus nicht bereitgestellt wird), wird es im standardenumerationsmodus erstellt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. An <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arSTR_FILE_SYS_BIND_DATA DisplayName</strong></a> zusammen mit <strong></strong>. Dadurch wird eine einfache-Verarbeitung erzwungen, während auch nach Desktop.ini Dateien entlang des Pfads gesucht wird, von dem eine lokalisierte namens Zeichenfolge zu erhalten ist. Dadurch wird die Überprüfung von Ordnern auf dem Pfad vermieden, was in einem Ordner, der einen Server oder eine Freigabe darstellt, viel Zeit und Ressourcen in Anspruch nehmen kann. Desktop.ini Dateien werden an einigen Speicherorten zwischengespeichert, sodass Sie mindestens so effizient sind wie das Durchsuchen von Ordner Attributen und die Suche nach der Desktop.ini, wenn der Ordner ou tot als schreibgeschützt aktivieren soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP SP2</strong>. Legen Sie diesen Bindungs Kontext fest, um eine Ordner Verknüpfung zum Auflösen der Verknüpfung zu erzwingen, die auf das Ziel verweist. <br/> Eine Ordner Verknüpfung ist ein Ordner Element, das auf ein anderes Ordner Element im selben Namespace zeigt, wobei eine Verknüpfung (Verknüpfung) verwendet wird, um die idlist des Ziels zu speichern. Der Link wird aufgelöst, um das Ziel zu verfolgen, wenn es verschoben oder umbenannt wird. Beispielsweise können der Ordner "Windows XP <strong>My Network Places</strong> " und der Ordner "Windows Vista <strong>Computer</strong> " Ordner Verknüpfungen enthalten, die mit dem Assistenten zum <strong>Hinzufügen von Netzwerk</strong> Adressen erstellt wurden. Um die Leistung zu verbessern, werden von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindTo Object</strong></a> -Methode standardmäßig keine Verknüpfungen zum Netzwerkordner aufgelöst.<br/> Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> oder <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: bindtohandler</strong></a>verwendet. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Legen Sie diesen Bindungs Kontext fest, um zu verhindern, dass ein Aufrufe der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode im <strong>Desktop</strong> Ordner relative Pfade relativ zum Desktop behandelt. in einem solchen Fall schlägt die Verarbeitung fehl, wenn dieser Bindungs Kontext angegeben wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um ein <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> anzuweisen, das Verknüpfungs Ziel nicht aufzulösen, das bei Verwendung der <strong>BHID_LinkTargetItem</strong> GUID in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: bindtohandler</strong></a>abgerufen wurde.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungs Kontext an, um Datei Metadaten für die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode bereitzustellen. diese Methode wird verwendet, anstatt zu versuchen, die eigentlichen Datei Metadaten abzurufen. Das zugeordnete-Objekt muss <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>ifilesystembinddata</strong></a> implementieren und optional auch <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>implementieren. Standardmäßig überprüft die <strong>IShellFolder::P arsetdisplayname</strong> -Methode, ob die Datei vorhanden ist, und verwendet die eigentlichen Metadaten der Datei, um die ID-Liste aufzufüllen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Wurde in Windows 8.1 eingeführt</strong>. Geben Sie diesen Bindungs Kontext an, um anzugeben, dass die im <strong>STR_FILE_SYS_FIND_DATA</strong> Bindungs Kontext bereitgestellten Daten verwendet werden sollen, um eine Itemid-Liste im Windows 7-Format zu erstellen.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungs Kontext an, wenn der Handler im gleichen Thread wie die Benutzeroberfläche abgerufen wird. Alle Arbeitsspeicher intensiven Aktivitäten, z. b. Datenträger-oder Netzwerk Zugriffe, sollten vermieden werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> -oder <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Handler anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindtoken Object</strong></a>verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> -Flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> -oder <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Handler anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindtoken Object</strong></a>verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> -Flag.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> -oder <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Handler anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindtoken Object</strong></a>verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> -Flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> -oder <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Handler anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindtoken Object</strong></a>verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> -Flag.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungs Kontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> -oder <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Handler anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindtoken Object</strong></a>verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> -Flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> -oder <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> -Handler anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: bindtoken Object</strong></a>verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> -Flag.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Nur Windows Vista.</strong> Geben Sie diesen Bindungs Kontext an, um einen Aufrufen der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> -Methode auszulösen, die die <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> -Schnittstelle für ein Dateisystem Objekt anfordert, einen Textfilter zurückzugeben, wenn kein anderer Filter verfügbar ist. Dieser Wert ist nicht als von Windows 7 definiert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Nur Windows Vista.</strong> Geben Sie diesen Bindungs Kontext an, um einen Aufrufen der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> -Methode auszulösen, der die <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> -Schnittstelle für ein Dateisystem Objekt anfordert, keinen Fall Back Filter zurückzugeben, wenn kein registrierter Filter gefunden werden konnte.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um das Laden des Verlaufs aus einem Stream für eine interne Navigation zu aktivieren, wenn die <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>ipersisthistory:: LoadHistory</strong></a> -Methode aufgerufen wird. Eine interne Navigation ist eine Navigation innerhalb derselben Ansicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungs Kontext mit STR_PARSE_PREFER_FOLDER_BROWSING an, wenn der Client die Internet Shell-Ordner Handler für eine beliebige gültige URL generieren möchte, wenn ein Ordner vom Typ DAV nicht für diese URL erstellt werden kann. Die URL kann nicht überprüft werden, weil Sie vorhanden ist. nur die Syntax wird geprüft, und Sie verfügt über einen registrierten Protokollhandler.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungs Kontext an, um Implementierungen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder anzuweisen::P arsedisplayname</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: initializeex</strong></a> , um speicherintensive Hilfsobjekte zwischenzuspeichern, die über Instanziierungen von shellelementen hinweg vorhanden sein können, anstatt diese Objekte bei jeder Erstellung eines shellelements neu zu erstellen. Das zugeordnete-Objekt ist ein weiteres Bindungs Kontext Objekt, das anfänglich leer ist. Dies sollte zu einem separaten Bindungs Kontext Objekt führen, das über <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a> oder <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: Register. objectparam</strong></a>aufgerufen wird. <br/> Ein Aufrufer muss dieses Verhalten durch Angabe dieses Bindungs Kontext Parameters beim Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>shcreateitemfromparametersingname</strong></a>Unternehmen. Auf diese Weise können Sie das Verhalten der Bindung an mehrere erteilungsnamen in Folge optimieren. Die Lebensdauer des Bindungs Kontext Objekts sollte mehrere Instanzen von shellelementen und Ihre individuellen Bindungs Kontexte umfassen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, damit ungültige Dateinamen Zeichen in Dateinamen angezeigt werden. Standardmäßig weist ein Aufrufe der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P armendisplayname</strong></a> -Methode Zeichen zurück, die in Dateinamen nicht zulässig sind. Dieser Bindungs Kontext ist nur in Verbindung mit dem STR_FILE_SYS_FIND_DATA Bindungs Kontext sinnvoll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um einen aufzurufenden <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P ar\displayname</strong></a> -Methode für den <strong>Desktop</strong> Ordner zum Analysieren von URLs zu aktivieren. Wenn dieser Bindungs Kontext angegeben wird, überschreibt er <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Legen Sie diesen Bindungs Kontext fest, um die Implementierung von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder (ishell:P Folder</strong></a> ) einer Datenquelle anzuweisen, um das Verhalten von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>shkreateitemfromparametersingname</strong></a>zu optimieren. <br/> Normalerweise führt <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>shkreateitemfromparamenername</strong></a> zwei Bindungs Vorgänge für den zu analysierten Namen aus: einen bis und einen bis zu <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsec Display Name</strong></a> und einen zum Erstellen des shellelements. Wenn der <strong>STR_PARSE_AND_CREATE_ITEM</strong> Bindungs Kontext unterstützt wird, wird die zweite Bindung vermieden, indem das shellelement während der <strong>IShellFolder::P arsedisplayname</strong> -Bindung erstellt und das shellelement über <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>iziseandkreateitem:: SetItem</strong></a>gespeichert wird. " <strong>Shkreateitemfromparser Name</strong> " verwendet dann das gespeicherte shellelement, anstatt eine zu erstellen.<br/> Dieser Parameter gilt für das letzte Element des Namens, der analysiert wird. Im &quot;C:\Folder1\File.txt Name werden die Daten beispielsweise auf File.txt angewendet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Nur Windows Vista.</strong> Geben Sie an, dass für diesen Bindungs Kontext beim Durchführen einer URL nicht die URL vorhanden sein muss, bevor eine idlist für die URL erzeugt wird. Geben Sie diesen Bindungs Kontext zusammen mit <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> an, wenn der Client wünscht, dass die <strong>Internet Shell</strong> -Ordner Handler eine idlist für die URL generieren, wenn für die angegebene URL kein DAV-Ordner erstellt werden kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um das ursprüngliche Element zu übergeben, das erneut analysiert wird, wenn dieses Element als <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> -Objekt gespeichert wird, das auch die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>iparameentanditem</strong></a> -Schnittstelle implementiert. Vor Windows 7 wurde dieser Wert nicht in einer Header Datei definiert. Er könnte vom Aufrufer definiert oder als sein Zeichen folgen Wert von " <strong>L &quot; para originalItem &quot; </strong>" übergeben werden. Ab Windows 7 wird der Wert in "shlobj. h" definiert. Beachten Sie, dass es sich hierbei um einen anderen Header als die anderen Str-Konstanten handelt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungs Kontext an, um einen Aufrufe der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode für den <strong>Desktop</strong> Ordner zu aktivieren, um URLs so zu analysieren, als wären Sie Ordner. Verwenden Sie diesen Bindungs Kontext zum Binden an einen WebDAV-Server.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Legen Sie diesen Bindungs Kontext fest, um zu verhindern, dass die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode auf dem Formular zum Auswerten von URLs des <strong>Desktop</strong> Ordners angezeigt wird. Dieser Bindungs Kontext kann von <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>überschrieben werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um den von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode verwendeten Standard Eigenschafts Speicher zu überschreiben, und verwenden Sie stattdessen den Eigenschaften Speicher, der als Bindungs Parameter angegeben ist. Gilt für delegatordner.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP SP2</strong>. Geben Sie diesen Bindungs Kontext an, um einen Aufrufen der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> -Methode für den <strong>Desktop</strong> Ordner zu aktivieren, um die " &quot; Shell: prefix"- &quot; Notation für den Zugriff auf Dateien zu verwenden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um einen Aufrufen der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> -Methode zu bewirken, dass das Dialogfeld für die Netzwerk Diagnose angezeigt wird, wenn die Analyse eines Netzwerk Pfads fehlschlägt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungs Kontext an, um einen Aufrufen der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode zu überspringen, um die Überprüfung des Netzwerkfreigabe Caches zu überspringen und den Netzwerkserver direkt zu kontaktieren. Informationen zu Netzwerkfreigaben werden zwischengespeichert, um die Leistung zu verbessern, und <strong>IShellFolder::P argdisplayname</strong> überprüft diesen Cache standardmäßig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungs Kontext an, um analysierte Eigenschaften an die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arandisplayname</strong></a> -Methode für einen delegatnamespace zu übergeben. Der Namespace kann die bestandenen Eigenschaften verwenden, anstatt zu versuchen, den Namen selbst zu analysieren.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Nur Windows Vista.</strong> Ein Analyse Bindungs Kontext, der verwendet wird, um einen Satz von Eigenschaften und den Namen des Elements beim Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>zu übergeben. Das Objekt im Bindungs Kontext implementiert <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> und wird durch Aufrufen von <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a>abgerufen.<br/> Dbfolder ist eine Shell-Datenquelle, die Elemente in Suchergebnissen und Abfrage basierten Sichten darstellt. Dbfolder ruft diese Elemente durch Abfragen des Windows Search-Systems ab. Elemente in den Suchergebnissen werden über ein Protokoll Schema identifiziert, z &quot; . b. "file:" oder " &quot; &quot; MAPI:" &quot; . Dbfolder bietet das Verhalten für diese Elemente, indem an Shell-Datenquellen delegiert wird, die für diese Protokolle erstellt werden. Weitere Informationen finden <a href="/previous-versions/bb233544(v=msdn.10)">Sie unter Entwickeln von Protokoll Handler-Add-ins</a> .<br/> Wenn dbfolder den Erstellungs Vorgang an die shelldatenquellen delegiert, die Windows Search-Protokolle unterstützen, bietet dieser Bindungs Kontext Zugriff auf Werte, die im Abfrageergebnis für dieses Element zurückgegeben wurden. Hierzu gehören folgende Elemente:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System. ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System. paramesingpath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System. itempathdisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System. itemnamedisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Dieser Bindungs Kontext kann auch verwendet werden, um ein dbfolder-Element zu analysieren, wenn ein Client über einen Satz von Eigenschaften verfügt, mit denen das Element definiert wird. In diesem Fall sollte ein leerer Name an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P argdisplayname</strong></a>-Element übermittelt werden.<br/> Vor Windows 7 wurde dieser Wert nicht in einer Header Datei definiert. Er könnte vom Aufrufer definiert oder als Zeichen folgen Wert übergeben werden: <code>L&quot;ParseWithProperties&quot;</code> . Ab Windows 7 wird der Wert in "shlobj. h" definiert. Beachten Sie, dass es sich hierbei um einen anderen Header handelt, als wenn die anderen Str-Konstanten definiert werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 8</strong>. Geben Sie diesen Bindungs Kontext an, um anzugeben, dass der Bindungs Kontext Parameter ein Eigenschaften Behälter (<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)"><strong>IPropertyBag</strong></a>) ist, der verwendet wird, um Variant-Werte im Bindungs Kontext zu übergeben. Weitere Informationen finden Sie im Abschnitt "Hinweise".<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungs Kontext an, um Aufrufe an die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> -Methode oder die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> -Methode zu veranlassen, eine bestimmte Shell-Namespace Erweiterung bei der Analyse oder Bindung zu ignorieren. Die CLSID des zu ignorierenden Namespace wird von der <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>ipersistent:: GetClassID-</strong></a> Methode des Bind-Parameters bereitgestellt. <br/>
<blockquote>
[!Note]<br />
Dieser Wert wurde in Windows 2000 SP3 eingeführt und wurde in shlobj. h bis Windows XP definiert, als er zu "shobjidl. h" verschoben wurde.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">Nicht verwendet.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Bindungs Kontexte werden verwendet, um optionale Parameter an Funktionen zu übergeben, die einen IBindCtx- \* Parameter aufweisen. Diese Parameter werden als COM-Objekte ausgedrückt und implementieren möglicherweise Schnittstellen, die verwendet werden, um die Parameterdaten zu modellieren. Einige Bindungs Kontexte stellen einen booleschen Wert dar, wobei **true** ein Objekt angibt, das nur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) implementiert, und false gibt an, dass kein Objekt vorhanden ist.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) und [**IShellItem:: bindtohandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) nehmen einen Bindungs Kontext an und können Ihnen Parameter über diesen Bindungs Kontext übergeben.

Einige Bindungs Kontexte sind für bestimmte Datenquellen Implementierungen oder Handlertypen spezifisch.

Bindungs Kontext Parameter werden für die Verwendung mit einer bestimmten Funktion oder Methode definiert.

Wenn Sie einen Eigenschafts Speicher über [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)anfordern, können Sie das Äquivalent [**von \_ GPS default**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) angeben, indem Sie einen NULL [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) -Parameter übergeben. Sie können auch die Entsprechung von GPS- \_ Lese schreiben angeben, indem Sie im Bindungs Kontext einen Modus von STGM- \_ Lesewert " \| STGM exklusiv" übergeben \_ .

Der vom **Str \_ PropertyBag \_ param** BIND-Kontext Objekt angegebene Eigenschaften Behälter enthält zusätzliche Werte, auf die Sie mit den Methoden [**IPropertyBag:: Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) und [**IPropertyBag:: Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) zugreifen können.



| Eigenschaftenname                                 | type     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Str \_ Enum \_ Items- \_ Flags                       | VT \_ UI4  | **Eingeführt in Windows 8**. Gibt einen [**shcontf**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) -Wert an, der an [**IShellFolder:: erumubjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) übergeben werden soll, wenn [**IShellItem:: bindtohandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) mit **bhid- \_ enumermen** aufgerufen wird.                                                                                                                                                                                                                         |
| die explizite Zuordnung der Str-Analyse war \_ \_ \_ \_ erfolgreich. | VT \_ bool | **Eingeführt in Windows 7**. Die [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) -Methode legt diese Eigenschaft fest, um dem Aufrufer mitzuteilen, dass die zurückgegebene idlist an die [ProgID](fa-progids.md) gebunden wurde, die mit Str-Analyse mit **\_ \_ \_ expliziter \_ ProgID** angegeben wurde, oder mit der mit Str Analyse angegebenen Anwendung **\_ \_ mit \_ expliziten \_ assocapp**. Wenn die explizite Zuordnung der Str-Analyse fehlt, wurde die ProgID oder Anwendung nicht an die idlist gebunden. **\_ \_ \_ \_** |
| Str-Analyse \_ \_ mit \_ expliziten \_ assocapp          | VT \_ BSTR | **Eingeführt in Windows 7**. Legen Sie diese Eigenschaft fest, um einen Rückruf der [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) -Methode zu bewirken, dass eine an den Dateityp-Zuordnungs Handler für die Anwendung gebundene idlist zurückgegeben wird.                                                                                                                                                                                                                                          |
| Str-Analyse \_ \_ mit \_ expliziter \_ ProgID            | VT \_ BSTR | **Eingeführt in Windows 7**. Legen Sie diese Eigenschaft fest, um einen Rückruf der [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) -Methode zu bewirken, dass eine idlist zurückgegeben wird, die an den Datei Zuordnungs Handler der bereitgestellten [ProgID](fa-progids.md)gebunden ist.                                                                                                                                                                                                                          |



 

Ein Beispiel für die Verwendung von Bindungs Kontext Werten finden Sie im Beispiel zum Auswerten [mit Parametern](samples-parsingwithparameters.md) .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 

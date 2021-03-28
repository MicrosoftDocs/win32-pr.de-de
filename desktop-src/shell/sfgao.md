---
description: Attribute, die für ein Element (Datei oder Ordner) oder eine Gruppe von Elementen abgerufen werden können.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: Sfgao (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f01691c3dbb1e5b76d93739b4893ffaf7c69e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757723"
---
# <a name="sfgao"></a>Sfgao

Attribute, die für ein Element (Datei oder Ordner) oder eine Gruppe von Elementen abgerufen werden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl> <dt><strong>SFGAO_CANCOPY</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente können kopiert werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl> <dt><strong>SFGAO_CANMOVE</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente können verschoben werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl> <dt><strong>SFGAO_CANLINK</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Verknüpfungen können für die angegebenen Elemente erstellt werden. Dieses Attribut hat denselben Wert wie <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br/> Wenn eine Namespace Erweiterung dieses Attribut zurückgibt, wird dem Kontextmenü, das bei Drag & Drop-Vorgängen angezeigt wird, ein <strong>Create Shortcut</strong> -Eintrag mit einem Standard Handler hinzugefügt. Die Erweiterung kann auch einen eigenen Handler für das <em>linkverb</em> anstelle der Standardeinstellung implementieren. Wenn die Erweiterung Dies bewirkt, ist Sie für das Erstellen der Verknüpfung verantwortlich.<br/> Außerdem wird dem Menü <strong>Datei</strong> in Windows-Explorer und normalen Kontextmenüs ein Verknüpfungs Element <strong>Erstellen</strong> hinzugefügt.<br/> Wenn das Element ausgewählt ist, wird die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu:: InvokeCommand</strong></a> -Methode der Anwendung mit dem <strong>lpverb</strong> -Member der <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>cminvokecommandinfo</strong></a> -Struktur aufgerufen, die auf <em>Link</em>festgelegt ist. Ihre Anwendung ist dafür verantwortlich, den Link zu erstellen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl> <dt><strong>SFGAO_STORAGE</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente können über <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindTo Object</strong></a>an ein <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a> -Objekt gebunden werden. Weitere Informationen zu den Funktionen der Namespace Bearbeitung finden Sie unter <strong>IStorage</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl> <dt><strong>SFGAO_CANRENAME</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente können umbenannt werden. Beachten Sie, dass dieser Wert im Grunde ein Vorschlag ist. die Umbenennung von Elementen durch nicht alle Namespace Clients ist möglich. Für diejenigen, für die dieses Attribut festgelegt werden muss.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl> <dt><strong>SFGAO_CANDELETE</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente können gelöscht werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl> <dt><strong>SFGAO_HASPROPSHEET</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente verfügen über Eigenschaften Blätter.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl> <dt><strong>SFGAO_DROPTARGET</strong></dt> <dt>0x00000100</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente sind Drop-Ziele.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl> <dt><strong>SFGAO_CAPABILITYMASK</strong></dt> <dt>0x00000177</dt> </dl></td>
<td style="text-align: left;">Dieses Flag ist eine Maske für die Funktions Attribute: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET und SFGAO_DROPTARGET. Aufrufer verwenden diesen Wert normalerweise nicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl> <dt><strong>SFGAO_SYSTEM</strong></dt> <dt>0x00001000</dt> </dl></td>
<td style="text-align: left;"><strong>Windows 7 und</strong>höher. Die angegebenen Elemente sind Systemelemente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl> <dt><strong>SFGAO_ENCRYPTED</strong></dt> <dt>0x00002000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente sind verschlüsselt und erfordern möglicherweise eine besondere Präsentation.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl> <dt><strong>SFGAO_ISSLOW</strong></dt> <dt>0x00004000</dt> </dl></td>
<td style="text-align: left;">Der Zugriff auf das Element (über <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> oder andere Speicher Schnittstellen) wird als langsamer Vorgang erwartet. Anwendungen sollten nicht auf Elemente zugreifen, die mit SFGAO_ISSLOW gekennzeichnet sind. <br/>
<blockquote>
[!Note]<br />
Das Öffnen eines Datenstroms für ein Element ist in der Regel ein langsamer Vorgang. SFGAO_ISSLOW gibt an, dass dies besonders langsam ist, z. b. bei langsamen Netzwerkverbindungen oder Offline Dateien (FILE_ATTRIBUTE_OFFLINE). Die Abfrage SFGAO_ISSLOW ist jedoch selbst ein langsamer Vorgang. Anwendungen sollten SFGAO_ISSLOW nur in einem Hintergrund Thread Abfragen. Anstelle eines Methoden Aufrufs, der SFGAO_ISSLOW umfasst, kann eine alternative Methode verwendet werden, z. b. das Abrufen der <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> -Eigenschaft und das Testen von FILE_ATTRIBUTE_OFFLINE.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl> <dt><strong>SFGAO_GHOSTED</strong></dt> <dt>0x00008000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente werden für den Benutzer als abgeblendete und nicht verfügbar angezeigt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl> <dt><strong>SFGAO_LINK</strong></dt> <dt>0x00010000 bis</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente sind Verknüpfungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl> <dt><strong>SFGAO_SHARE</strong></dt> <dt>0x00020000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Objekte werden freigegeben.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl> <dt><strong>SFGAO_READONLY</strong></dt> <dt>0x00040000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente sind schreibgeschützt. Im Fall von Ordnern bedeutet dies, dass in diesen Ordnern keine neuen Elemente erstellt werden können. Dies sollte nicht mit dem Verhalten verwechselt werden, das durch das FILE_ATTRIBUTE_READONLY-Flag angegeben wird, das von <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>icolumnprovider:: GetItemData</strong></a> in einer <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>shcolumndata</strong></a> -Struktur abgerufen wird. FILE_ATTRIBUTE_READONLY hat keine Bedeutung für Win32-Dateisystem Ordner.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl> <dt><strong>SFGAO_HIDDEN</strong></dt> <dt>0x00080000</dt> </dl></td>
<td style="text-align: left;">Das Element ist ausgeblendet und sollte nur angezeigt werden, wenn die Option Ausgeblendete <strong>Dateien und Ordner anzeigen</strong> in den <strong>Ordner Einstellungen</strong>aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl> <dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt> <dt>0x000fc000</dt> </dl></td>
<td style="text-align: left;">Darf nicht verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl> <dt><strong>SFGAO_NONENUMERATED</strong></dt> <dt>0x00100000</dt> </dl></td>
<td style="text-align: left;">Die Elemente sind nicht aufgelistete Elemente und sollten ausgeblendet werden. Sie werden nicht durch einen Enumerator zurückgegeben, wie z. b. der, der von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: erumubjects</strong></a> -Methode erstellt wurde.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl> <dt><strong>SFGAO_NEWCONTENT</strong></dt> <dt>0x00200000</dt> </dl></td>
<td style="text-align: left;">Die Elemente enthalten neuen Inhalt, wie von der jeweiligen Anwendung definiert.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl> <dt><strong>SFGAO_CANMONIKER</strong></dt> </dl></td>
<td style="text-align: left;">Wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl> <dt><strong>SFGAO_HASSTORAGE</strong></dt> </dl></td>
<td style="text-align: left;">Wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl> <dt><strong>SFGAO_STREAM</strong></dt> <dt>0x00400000</dt> </dl></td>
<td style="text-align: left;">Gibt an, dass dem Element ein Stream zugeordnet ist. Auf diesen Stream kann durch Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> oder <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: bindtohandler</strong></a> mit IID_IStream im <em>riid</em> -Parameter zugegriffen werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl> <dt><strong>SFGAO_STORAGEANCESTOR</strong></dt> <dt>0x00800000</dt> </dl></td>
<td style="text-align: left;">Untergeordnete Elemente dieses Elements sind über <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> oder <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>zugänglich. Diese untergeordneten Elemente werden mit SFGAO_STORAGE oder SFGAO_STREAM gekennzeichnet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl> <dt><strong>SFGAO_VALIDATE</strong></dt> <dt>0x01000000</dt> </dl></td>
<td style="text-align: left;">Bei Angabe als Eingabe weist SFGAO_VALIDATE den Ordner an, zu überprüfen, ob die Elemente in einem Ordner oder shellelementarray vorhanden sind. Wenn mindestens eines dieser Elemente nicht vorhanden ist, geben <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder:: getattributesof</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>ishellitemarray:: GetAttributes</strong></a> einen Fehlercode zurück. Dieses Flag wird nie als [out]-Wert zurückgegeben.<br/> Bei der Verwendung mit dem Dateisystem Ordner weist SFGAO_VALIDATE den Ordner an, zwischengespeicherte Eigenschaften zu verwerfen, die von Clients von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2:: getdetailsex</strong></a> abgerufen wurden, die möglicherweise für die angegebenen Elemente angesammelt wurden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl> <dt><strong>SFGAO_REMOVABLE</strong></dt> <dt>0x02000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente befinden sich auf einem Wechsel Datenträger oder selbst Wechselmedien.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl> <dt><strong>SFGAO_COMPRESSED</strong></dt> <dt>0x04000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente werden komprimiert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl> <dt><strong>SFGAO_BROWSABLE</strong></dt> <dt>0x08000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente können in einem Webbrowser oder Windows Explorer-Frame gehostet werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl> <dt><strong>SFGAO_FILESYSANCESTOR</strong></dt> <dt>0x10000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Ordner sind entweder Dateisystem Ordner oder enthalten mindestens einen Nachfolger (untergeordnetes Element, ein untergeordnetes Element oder später), bei dem es sich um einen Dateisystem Ordner (SFGAO_FILESYSTEM) handelt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl> <dt><strong>SFGAO_FOLDER</strong></dt> <dt>0x20000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Elemente sind Ordner. Einige Elemente können mit SFGAO_STREAM und SFGAO_FOLDER gekennzeichnet werden, z. b. mit einer komprimierten Datei mit der Dateinamenerweiterung ". zip". Einige Anwendungen können dieses Flag enthalten, wenn Sie auf Elemente testen, bei denen es sich um Dateien und Container handelt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl> <dt><strong>SFGAO_FILESYSTEM</strong></dt> <dt>0x40000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Ordner oder Dateien sind Teil des Dateisystems (d. h. Dateien, Verzeichnisse oder Stamm Verzeichnisse). Die analysierten Namen der Elemente können als gültige Win32-Dateisystem Pfade angesehen werden. Diese Pfade können entweder UNC oder auf Laufwerk Buchstaben basieren.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl> <dt><strong>SFGAO_STORAGECAPMASK</strong></dt> <dt>0x70c50008</dt> </dl></td>
<td style="text-align: left;">Dieses Flag ist eine Maske für die Speicher Funktions Attribute: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER und SFGAO_FILESYSTEM. Aufrufer verwenden diesen Wert normalerweise nicht.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl> <dt><strong>SFGAO_HASSUBFOLDER</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Die angegebenen Ordner enthalten Unterordner. Das SFGAO_HASSUBFOLDER-Attribut ist nur eine Empfehlung und kann von shellordnerimplementierungen zurückgegeben werden, auch wenn Sie keine Unterordner enthalten. Beachten Sie jedoch, dass der umgekehrte –, der SFGAO_HASSUBFOLDER nicht zurückgibt – definitiv angibt, dass die Ordner Objekte nicht über Unterordner verfügen.<br/> Die Rückgabe von SFGAO_HASSUBFOLDER wird empfohlen, wenn eine beträchtliche Zeitspanne erforderlich ist, um zu bestimmen, ob Unterordner vorhanden sind. Beispielsweise gibt die Shell immer SFGAO_HASSUBFOLDER zurück, wenn sich ein Ordner auf einem Netzwerklaufwerk befindet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl> <dt><strong>SFGAO_CONTENTSMASK</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Dieses Flag ist eine Maske für Inhalts Attribute, derzeit nur SFGAO_HASSUBFOLDER. Aufrufer verwenden diesen Wert normalerweise nicht.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl> <dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt> <dt>0x81044000</dt> </dl></td>
<td style="text-align: left;">Maske, die von der <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> -Eigenschaft verwendet wird, um Attribute zu bestimmen, die für langsame Berechnungen oder einen fehlenden Kontext gelten: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER und SFGAO_VALIDATE. Aufrufer verwenden diesen Wert normalerweise nicht.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IShellFolder:: getattributesof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder::P aramdisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**Ishellitemarray:: GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 

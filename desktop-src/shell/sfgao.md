---
description: Attribute, die für ein Element (Datei oder Ordner) oder eine Gruppe von Elementen abgerufen werden können.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: SFGAO (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ae5dca355b7c22e3075a0ced7640a5bd45a54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481986"
---
# <a name="sfgao"></a>SFGAO

Attribute, die für ein Element (Datei oder Ordner) oder eine Gruppe von Elementen abgerufen werden können.




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl><dt><strong>SFGAO_CANCOPY</strong></dt><dt>0x00000001</dt></dl> | Die angegebenen Elemente können kopiert werden.<br /> | 
| <span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl><dt><strong>SFGAO_CANMOVE</strong></dt><dt>0x00000002</dt></dl> | Die angegebenen Elemente können verschoben werden.<br /> | 
| <span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl><dt><strong>SFGAO_CANLINK</strong></dt><dt>0x00000004</dt></dl> | Verknüpfungen können für die angegebenen Elemente erstellt werden. Dieses Attribut hat den gleichen Wert wie <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br /> If a namespace extension returns this attribute, a <strong>Create Shortcut</strong> entry with a default handler is added to the shortcut menu that is displayed during drag-and-drop operations. Die Erweiterung kann auch einen eigenen Handler für das <em>Linkverb</em> anstelle des Standardwerts implementieren. Wenn die Erweiterung dies tut, ist sie für die Erstellung der Verknüpfung verantwortlich.<br /> Dem Menü Windows <strong>Explorer-Datei</strong> und normalen Kontextmenüs wird auch ein Element Verknüpfung <strong>erstellen</strong> hinzugefügt.<br /> Wenn das Element ausgewählt ist, wird die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand-Methode</strong></a> Ihrer Anwendung aufgerufen, wobei der <strong>lpVerb-Member</strong> der <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO-Struktur</strong></a> festgelegt ist, um zu <em>verknüpfen.</em> Ihre Anwendung ist für die Erstellung des Links verantwortlich.<br /> | 
| <span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl><dt><strong>SFGAO_STORAGE</strong></dt><dt>0x00000008</dt></dl> | Die angegebenen Elemente können über <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>an ein <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage-Objekt</strong></a> gebunden werden. Weitere Informationen zu Namespace-Manipulationsfunktionen finden Sie unter <strong>IStorage</strong>.<br /> | 
| <span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl><dt><strong>SFGAO_CANRENAME</strong></dt><dt>0x00000010</dt></dl> | Die angegebenen Elemente können umbenannt werden. Beachten Sie, dass dieser Wert im Wesentlichen ein Vorschlag ist. Nicht alle Namespaceclients lassen das Umbenennen von Elementen zu. Für diejenigen, für die dieses Attribut festgelegt ist, muss jedoch festgelegt sein.<br /> | 
| <span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl><dt><strong>SFGAO_CANDELETE</strong></dt><dt>0x00000020</dt></dl> | Die angegebenen Elemente können gelöscht werden.<br /> | 
| <span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl><dt><strong>SFGAO_HASPROPSHEET</strong></dt><dt>0x00000040</dt></dl> | Die angegebenen Elemente verfügen über Eigenschaftenblätter.<br /> | 
| <span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl><dt><strong>SFGAO_DROPTARGET</strong></dt><dt>0x00000100</dt></dl> | Die angegebenen Elemente sind Ablageziele.<br /> | 
| <span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl><dt><strong>SFGAO_CAPABILITYMASK</strong></dt><dt>0x00000177</dt></dl> | Dieses Flag ist eine Maske für die Funktionsattribute: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET und SFGAO_DROPTARGET. Aufrufer verwenden diesen Wert normalerweise nicht.<br /> | 
| <span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl><dt><strong>SFGAO_SYSTEM</strong></dt><dt>0x00001000</dt></dl> | <strong>Windows 7 und höher.</strong> Die angegebenen Elemente sind Systemelemente.<br /> | 
| <span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl><dt><strong>SFGAO_ENCRYPTED</strong></dt><dt>0x00002000</dt></dl> | Die angegebenen Elemente werden verschlüsselt und erfordern möglicherweise eine besondere Darstellung.<br /> | 
| <span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl><dt><strong>SFGAO_ISSLOW</strong></dt><dt>0x00004000</dt></dl> | Der Zugriff auf das Element (über <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> oder andere Speicherschnittstellen) wird als langsamer Vorgang erwartet. Anwendungen sollten den Zugriff auf Elemente vermeiden, die mit SFGAO_ISSLOW gekennzeichnet sind. <br /><blockquote>[!Note]<br />Das Öffnen eines Datenstroms für ein Element ist in der Regel immer ein langsamer Vorgang. SFGAO_ISSLOW gibt an, dass er voraussichtlich besonders langsam ist, z. B. bei langsamen Netzwerkverbindungen oder Offlinedateien (FILE_ATTRIBUTE_OFFLINE). Das Abfragen von SFGAO_ISSLOW ist jedoch selbst ein langsamer Vorgang. Anwendungen sollten SFGAO_ISSLOW nur in einem Hintergrundthread abfragen. Eine alternative Methode, z. B. das Abrufen der <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes-Eigenschaft</strong></a> und das Testen auf FILE_ATTRIBUTE_OFFLINE, kann anstelle eines Methodenaufrufs verwendet werden, der SFGAO_ISSLOW umfasst.</blockquote><br /> | 
| <span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl><dt><strong>SFGAO_GHOSTED</strong></dt><dt>0x00008000</dt></dl> | Die angegebenen Elemente werden als abgeblendet angezeigt und sind für den Benutzer nicht verfügbar.<br /> | 
| <span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl><dt><strong>SFGAO_LINK</strong></dt><dt>0x00010000</dt></dl> | Die angegebenen Elemente sind Verknüpfungen.<br /> | 
| <span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl><dt><strong>SFGAO_SHARE</strong></dt><dt>0x00020000</dt></dl> | Die angegebenen Objekte werden freigegeben.<br /> | 
| <span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl><dt><strong>SFGAO_READONLY</strong></dt><dt>0x00040000</dt></dl> | Die angegebenen Elemente sind schreibgeschützt. Im Fall von Ordnern bedeutet dies, dass in diesen Ordnern keine neuen Elemente erstellt werden können. Dies sollte nicht mit dem Verhalten verwechselt werden, das durch das von <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> in einer <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA-Struktur</strong></a> abgerufene FILE_ATTRIBUTE_READONLY-Flag angegeben wird. FILE_ATTRIBUTE_READONLY hat keine Bedeutung für Win32-Dateisystemordner.<br /> | 
| <span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl><dt><strong>SFGAO_HIDDEN</strong></dt><dt>0x00080000</dt></dl> | Das Element ist ausgeblendet und sollte nur angezeigt werden, wenn die Option <strong>Ausgeblendete Dateien und Ordner anzeigen</strong> in Ordner <strong>Einstellungen</strong>aktiviert ist.<br /> | 
| <span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt><dt>0x000FC000</dt></dl> | Darf nicht verwendet werden.<br /> | 
| <span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl><dt><strong>SFGAO_NONENUMERATED</strong></dt><dt>0x00100000</dt></dl> | Die Elemente sind nicht aufzählte Elemente und sollten ausgeblendet werden. Sie werden nicht über einen Enumerator wie den zurückgegeben, der von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder::EnumObjects-Methode</strong></a> erstellt wurde.<br /> | 
| <span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl><dt><strong>SFGAO_NEWCONTENT</strong></dt><dt>0x00200000</dt></dl> | Die Elemente enthalten neuen Inhalt, wie von der jeweiligen Anwendung definiert.<br /> | 
| <span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl><dt><strong>SFGAO_CANMONIKER</strong></dt></dl> | Wird nicht unterstützt.<br /> | 
| <span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl><dt><strong>SFGAO_HASSTORAGE</strong></dt></dl> | Wird nicht unterstützt.<br /> | 
| <span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl><dt><strong>SFGAO_STREAM</strong></dt><dt>0x00400000</dt></dl> | Gibt an, dass dem Element ein Stream zugeordnet ist. Auf diesen Stream kann über einen Aufruf von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> oder <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a> mit IID_IStream im <em>riid-Parameter</em> zugegriffen werden.<br /> | 
| <span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt><dt>0x00800000</dt></dl> | Auf untergeordnete Elemente dieses Elements kann über <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> oder <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>zugegriffen werden. Diese untergeordneten Elemente werden mit SFGAO_STORAGE oder SFGAO_STREAM gekennzeichnet.<br /> | 
| <span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl><dt><strong>SFGAO_VALIDATE</strong></dt><dt>0x01000000</dt></dl> | Bei Angabe als Eingabe weist SFGAO_VALIDATE den Ordner an, zu überprüfen, ob die in einem Ordner oder Shellelementarray enthaltenen Elemente vorhanden sind. Wenn mindestens eines dieser Elemente nicht vorhanden ist, geben <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder::GetAttributesOf</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray::GetAttributes</strong></a> einen Fehlercode zurück. Dieses Flag wird nie als [out]-Wert zurückgegeben.<br /> Bei Verwendung mit dem Dateisystemordner weist SFGAO_VALIDATE den Ordner an, zwischengespeicherte Eigenschaften zu verwerfen, die von Clients von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2::GetDetailsEx</strong></a> abgerufen wurden, die sich möglicherweise für die angegebenen Elemente angesammelt haben.<br /> | 
| <span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl><dt><strong>SFGAO_REMOVABLE</strong></dt><dt>0x02000000</dt></dl> | Die angegebenen Elemente befinden sich auf Wechselmedien oder selbst auf Wechselmedien.<br /> | 
| <span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl><dt><strong>SFGAO_COMPRESSED</strong></dt><dt>0x04000000</dt></dl> | Die angegebenen Elemente werden komprimiert.<br /> | 
| <span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl><dt><strong>SFGAO_BROWSABLE</strong></dt><dt>0x08000000</dt></dl> | Die angegebenen Elemente können in einem Webbrowser oder Windows Explorer-Frame gehostet werden.<br /> | 
| <span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt><dt>0x10000000</dt></dl> | Die angegebenen Ordner sind entweder Dateisystemordner oder enthalten mindestens einen Nachfolger (untergeordnetes Element, untergeordnetes Kind oder höher), bei dem es sich um einen Dateisystemordner (SFGAO_FILESYSTEM) handelt.<br /> | 
| <span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl><dt><strong>SFGAO_FOLDER</strong></dt><dt>0x20000000</dt></dl> | Die angegebenen Elemente sind Ordner. Einige Elemente können sowohl mit SFGAO_STREAM als auch mit SFGAO_FOLDER gekennzeichnet werden, z. B. mit einer komprimierten Datei mit .zip Dateinamenerweiterung. Einige Anwendungen können dieses Flag enthalten, wenn auf Elemente getestet wird, bei denen es sich sowohl um Dateien als auch um Container handelt.<br /> | 
| <span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl><dt><strong>SFGAO_FILESYSTEM</strong></dt><dt>0x40000000</dt></dl> | Die angegebenen Ordner oder Dateien sind Teil des Dateisystems (d. b. Dateien, Verzeichnisse oder Stammverzeichnisse). Es kann davon ausgegangen werden, dass die analysierten Namen der Elemente gültige Win32-Dateisystempfade sind. Diese Pfade können entweder UNC- oder laufwerkbuchstabebasiert sein.<br /> | 
| <span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl><dt><strong>SFGAO_STORAGECAPMASK</strong></dt><dt>0x70C50008</dt></dl> | Dieses Flag ist eine Maske für die Speicherfunktionsattribute SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER und SFGAO_FILESYSTEM. Aufrufer verwenden diesen Wert normalerweise nicht.<br /> | 
| <span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl><dt><strong>SFGAO_HASSUBFOLDER</strong></dt><dt>0x80000000</dt></dl> | Die angegebenen Ordner verfügen über Unterordner. Das SFGAO_HASSUBFOLDER-Attribut ist nur eine Empfehlung und wird möglicherweise von Shellordnerimplementierungen zurückgegeben, auch wenn sie keine Unterordner enthalten. Beachten Sie jedoch, dass die umgekehrte - nicht SFGAO_HASSUBFOLDER zurück gibt - definitiv an, dass die Ordnerobjekte keine Unterordner haben.<br /> Die SFGAO_HASSUBFOLDER wird immer dann empfohlen, wenn eine erhebliche Zeit benötigt wird, um zu bestimmen, ob Unterordner vorhanden sind. Die Shell gibt z. B. immer SFGAO_HASSUBFOLDER zurück, wenn sich ein Ordner auf einem Netzwerklaufwerk befindet.<br /> | 
| <span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl><dt><strong>SFGAO_CONTENTSMASK</strong></dt><dt>0x80000000</dt></dl> | Dieses Flag ist eine Maske für Inhaltsattribute, derzeit nur SFGAO_HASSUBFOLDER. Aufrufer verwenden diesen Wert normalerweise nicht.<br /> | 
| <span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt><dt>0x81044000</dt></dl> | Maskierung, die von der <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags-Eigenschaft</a> verwendet wird, um Attribute zu bestimmen, die als ursache langsamer Berechnungen oder fehlender Kontext angesehen werden: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER und SFGAO_VALIDATE. Aufrufer verwenden diesen Wert normalerweise nicht.<br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray::GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 

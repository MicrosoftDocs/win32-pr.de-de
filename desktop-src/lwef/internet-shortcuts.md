---
title: Internet Verknüpfungen
description: Das Internet-Verknüpfungs Objekt wird verwendet, um Desktop Verknüpfungen zu Internet Sites zu erstellen.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Internet-Verknüpfungs Objekte
- WebBrowser-Steuerelemente
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14bc2ed58f75522e59b9008ded7b0f1416a21fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038955"
---
# <a name="internet-shortcuts"></a>Internet Verknüpfungen

Das Internet-Verknüpfungs Objekt wird verwendet, um Desktop Verknüpfungen zu Internet Sites zu erstellen. Ebenso wie Verknüpfungen zu Elementen im Dateisystem verwenden Internet Verknüpfungen die Form eines Symbols auf dem Desktop. Wenn der Benutzer auf das Symbol klickt, wird der Browser gestartet und zeigt die Website an, die der Verknüpfung zugeordnet ist.

Die folgenden Themen werden erörtert.

-   [Erstellen von Internet Verknüpfungen](#creating-internet-shortcuts)
    -   [Erstellen einer Internet Verknüpfung über ein Webbrowser-Steuerelement](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Erstellen einer Internet Verknüpfung aus einer URL](#creating-an-internet-shortcut-from-a-url)
-   [Zugreifen auf Eigenschaften Speicher](#accessing-property-storage)
-   [Schnittstellen](#interfaces)
    -   [OLE-Schnittstellen](#ole-interfaces)
    -   [Shellschnittstellen](#shell-interfaces)
-   [Funktionen](#functions)
    -   [Funktionen des Internet-shortcututility](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Erstellen von Internet Verknüpfungen

Sie können eine Internet Verknüpfung erstellen, indem Sie ein Webbrowser-Steuerelement oder die URL der Seite verwenden.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Erstellen einer Internet Verknüpfung über ein Webbrowser-Steuerelement

Wenn die Anwendung ein Webbrowser-Steuerelement hostet, können Sie das Internet-Verknüpfungs Objekt verwenden, um Verknüpfungen auf folgende Weise zu erstellen.

1.  Erstellen Sie mithilfe eines Klassen Bezeichners (CLSID) von CLSID internetshortcut eine Instanz des Internet Verknüpfungs Objekts mit [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) \_ .
2.  Übergeben Sie den Zeiger an die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Browsers an das Internet-Verknüpfungs Objekt mit [IObjectWithSite:: SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Rufen Sie die [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) -Methode des Internet Verknüpfungs Objekts auf, wenn Sie eine Verknüpfung zu der Seite erstellen möchten, die vom Webbrowser-Steuerelement angezeigt wird.

Eine Verknüpfung wird an dem in [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)angegebenen Speicherort erstellt. Dieser Speicherort ermöglicht dem Webbrowser-Steuerelement, seinen Zustand wiederherzustellen. Dies schließt das Laden der korrekten Dokumente in Framesets ein.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Erstellen einer Internet Verknüpfung aus einer URL

Sie können auch eine Internet Verknüpfung erstellen, wenn Sie über die URL der Seite verfügen, mit der Sie eine Verknüpfung herstellen möchten.

1.  Erstellen Sie mithilfe einer CLSID von CLSID internetshortcut eine Instanz des Internet-Verknüpfungs Objekts mit [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) \_ .
2.  Verwenden Sie die [iuniforresourcelocator:: setURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) -Methode, um die URL in der Verknüpfung festzulegen.
3.  Verwenden Sie die [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) -Methode, um die Verknüpfungs Datei an einem gewünschten Speicherort zu speichern.

## <a name="accessing-property-storage"></a>Zugreifen auf Eigenschaften Speicher

Das Internet-Verknüpfungs Objekt enthält mehrere Eigenschaften, auf die Sie über die [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) -Schnittstelle des Objekts zugreifen können. verwenden Sie dazu das folgende Verfahren.

1.  Rufen Sie die [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) -Schnittstelle durch Aufrufen von [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) mit IID \_ IPropertySetStorage ab.
2.  Greifen Sie auf den Speicher Satz für die Internet Verknüpfungs Eigenschaft zu, indem Sie [IPropertySetStorage:: Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) mit fmtid \_ intshcut oder fmtid \_ Internetsite aufrufen, um die [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) -Schnittstelle zu erhalten.
3.  Lesen Sie die Eigenschaften Speicherinformationen mit [IPropertyStorage:: infomultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) , indem Sie die entsprechende eigen schafts-ID übergeben.

Bei [Version 4,70 oder höher](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) von Shell32.dll können Sie auch die [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) -Schnittstelle abrufen, indem Sie [**IShellFolder:: BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) aufrufen, wobei der *PIDL* -Parameter auf festgelegt ist. Die URL-Datei und der *riid* -Parameter sind auf IID \_ IPropertySetStorage festgelegt.

Die folgenden Eigenschaften-IDs können für fmtid \_ intshcut angefordert werden.



| PROPID               | Varianttyp | BESCHREIBUNG                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ ist \_ URL         | VT \_ LPWSTR   | Die URL, zu der die Verknüpfung führt             |
| PID \_ ist \_ Name        | VT \_ LPWSTR   | Name der Internet Verknüpfung               |
| PID \_ ist \_ workingdir  | VT \_ LPWSTR   | Arbeitsverzeichnis für die Verknüpfung          |
| PID \_ ist ein \_ Hotkey      | VT \_ UI2      | Hotkey für die Verknüpfung                     |
| PID \_ ist \_ ShowCmd     | VT \_ I4       | Befehl für Verknüpfung anzeigen                   |
| PID \_ ist \_ IconIndex   | VT \_ I4       | Index des Symbols                           |
| PID \_ ist \_ IconFile    | VT \_ LPWSTR   | Die Datei, die das Symbol enthält.                 |
| PID \_ ist " \_ What SNEW"    | VT \_ LPWSTR   | Neues Text                             |
| PID \_ ist \_ Autor      | VT \_ LPWSTR   | Autor                                      |
| PID \_ ist \_ Beschreibung | VT \_ LPWSTR   | Beschreibungstext der Site                    |
| PID \_ ist \_ Kommentar     | VT \_ LPWSTR   | Kommentar für Benutzer mit Anmerkungen                      |
| PID \_ ist \_ Roaming      | VT \_ bool     | True, wenn die Verknüpfung zum ersten Mal rostet |



 

Die folgenden Eigenschaften-IDs können für die fmtid \_ Internetsite angefordert werden.



| PROPID                     | Varianttyp | BESCHREIBUNG                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID- \_ intSite mit \_ Neuerungen     | VT \_ LPWSTR   | Neues Text                                   |
| PID- \_ intSite- \_ Autor       | VT \_ LPWSTR   | Autor                                            |
| PID \_ intSite \_ lastVisit    | VT \_ FILETIME | Uhrzeit des letzten Orts                        |
| PID \_ intSite \_ LastMod      | VT \_ FILETIME | Uhrzeit der letzten Änderung des Standorts                       |
| PID- \_ intSite \_ visitcount   | VT \_ UI4      | Anzahl der besuchten Benutzer                  |
| Beschreibung der PID- \_ intSite \_  | VT \_ LPWSTR   | Beschreibungstext der Site                          |
| PID \_ intSite- \_ Kommentar      | VT \_ LPWSTR   | Kommentar für Benutzer mit Anmerkungen                            |
| PID- \_ intSite- \_ Flags        | VT \_ UI4      | Gibt die Verwendung von pidisf- \_ Flags an (siehe unten).       |
| \_int-intSite- \_ contentlen   | –          | Derzeit nicht unterstützt                           |
| Code der PID- \_ intSite \_  | –          | Derzeit nicht unterstützt                           |
| PID- \_ intSite \_ Rekurse      | –          | Derzeit nicht unterstützt                           |
| PID \_ intSite \_ Watch        | –          | Derzeit nicht unterstützt                           |
| PID- \_ intSite- \_ Abonnement | VT \_ UI8      | Abonnementcookie-Wert für Abonnement-Manager |
| PID- \_ intSite- \_ URL          | VT \_ LPWSTR   | Die URL, zu der die Verknüpfung führt                   |
| Titel der PID- \_ intSite \_        | VT \_ LPWSTR   | Titel                                             |
| PID- \_ intSite- \_ Codepage     | VT \_ UI4      | Codepage des Dokuments                          |
| PID- \_ intSite-nach \_ Verfolgung     | –          | Derzeit nicht unterstützt                           |
| PID \_ intSite \_ IconIndex    | VT \_ I4       | Index des Symbols                                 |
| PID- \_ intSite \_ IconFile     | VT \_ LPWSTR   | Die Datei, die das Symbol enthält.                       |
| PID- \_ intSite \_ Roamed       | VT \_ UI4      | Der Eintrag wurde aufgrund des Roamings hinzugefügt.                |



 

Im folgenden finden Sie die Internet Site Flags.



| Flag                    | Beschreibung                                |
|-------------------------|--------------------------------------------|
| pidisf \_ recentlychanged | Gibt an, dass eine Site vor kurzem geändert wurde. |
| pidisf \_ cachedkurznotiz    | Derzeit nicht unterstützt                    |
| pidisf \_ cacheimages     | Derzeit nicht unterstützt                    |
| pidisf \_ Follow walllinks  | Derzeit nicht unterstützt                    |



 

Die folgenden Werte werden für den Internet roamingverlauf verwendet.



| Wert von PID \_ intSite \_ Roamed         | BESCHREIBUNG                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wert nicht festgelegt oder pidisr auf \_ \_ \_ dem neuesten Stand | Dieser Cache Eintrag wurde durch Roaming nicht geändert.                                                                                                                       |
| pidisr \_ benötigt \_ Hinzufügen                    | Dieser Cache Eintrag wurde durch Roaming zum Cache hinzugefügt. Legen Sie pidisr auf \_ \_ den \_ neuesten Stand, sobald die Verarbeitung des Eintrags beendet ist.                                                   |
| pidisr \_ benötigt \_ Update                 | Dieser Cache Eintrag war bereits auf dem lokalen Computer vorhanden, wurde aber durch Roaming aktualisiert. Legen Sie pidisr auf \_ \_ den \_ neuesten Stand, sobald die Verarbeitung des Eintrags beendet ist.                 |
| pidisr \_ muss \_ gelöscht werden                 | Das Roaming hat festgestellt, dass dieser Cache Eintrag gelöscht werden soll. Der Benutzer hat z. b. seinen Browserverlauf gelöscht. Löschen Sie den Eintrag mithilfe von deleteurlcacheentry. |



 

## <a name="interfaces"></a>Schnittstellen

Das Internet-Verknüpfungs Objekt macht eine Reihe von Schnittstellen verfügbar.

### <a name="ole-interfaces"></a>OLE-Schnittstellen

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Shellschnittstellen

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**Iextracticon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**Inewshortcuthook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**Ishellextinit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**Ishellpropsheetext**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**Iqueryinfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Functions

Es gibt mehrere Hilfsfunktionen, die mit dem Internet-Verknüpfungs Objekt verwendet werden können.

### <a name="internet-shortcut-utility-functions"></a>Funktionen des Internet-shortcututility

-   [**Inetisoffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**Mimeassociationdialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**Translateurl**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**Urlassociationdialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 
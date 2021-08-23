---
title: Internetverknüpfungen
description: Das Internetverknüpfungsobjekt wird verwendet, um Desktopverknüpfungen zu Internetsites zu erstellen.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Internetverknüpfungsobjekte
- WebBrowser-Steuerelemente
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aba53c320ed740fe7d91a2425b4d47d66e28d78aa35e4ce893efeed12380c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749408"
---
# <a name="internet-shortcuts"></a>Internetverknüpfungen

Das Internetverknüpfungsobjekt wird verwendet, um Desktopverknüpfungen zu Internetsites zu erstellen. Wie Verknüpfungen zu Elementen im Dateisystem haben Internetverknüpfungen die Form eines Symbols auf dem Desktop. Wenn der Benutzer auf das Symbol klickt, wird der Browser gestartet und zeigt die Website an, die der Verknüpfung zugeordnet ist.

Die folgenden Themen werden erläutert.

-   [Erstellen von Internetverknüpfungen](#creating-internet-shortcuts)
    -   [Erstellen einer Internetverknüpfung aus einem WebBrowser-Steuerelement](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Erstellen einer Internetverknüpfung über eine URL](#creating-an-internet-shortcut-from-a-url)
-   [Zugreifen auf Storage](#accessing-property-storage)
-   [Schnittstellen](#interfaces)
    -   [OLE-Schnittstellen](#ole-interfaces)
    -   [Shellschnittstellen](#shell-interfaces)
-   [Funktionen](#functions)
    -   [Funktionen des Hilfsprogramms "Internetverknüpfung"](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Erstellen von Internetverknüpfungen

Sie können eine Internetverknüpfung mithilfe eines WebBrowser-Steuerelements oder mit der URL der Seite erstellen.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Erstellen einer Internetverknüpfung aus einem WebBrowser-Steuerelement

Wenn Ihre Anwendung ein WebBrowser-Steuerelement hostet, können Sie das Internetverknüpfungsobjekt verwenden, um Verknüpfungen wie folgt zu erstellen.

1.  Erstellen Sie mit [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)eine Instanz des Internetverknüpfungsobjekts mithilfe eines Klassenbezeichners (CLSID) von CLSID \_ InternetShortcut.
2.  Übergeben Sie den Zeiger auf die [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) von WebBrowser mit [IObjectWithSite::SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)an das Internetverknüpfungsobjekt.
3.  Rufen Sie die [IPersistFile::Save-Methode](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) des Internetverknüpfungsobjekts auf, wenn Sie eine Verknüpfung mit der Seite erstellen möchten, die vom WebBrowser-Steuerelement angezeigt wird.

Eine Verknüpfung wird an dem in [IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)angegebenen Speicherort erstellt. An diesem Speicherort kann das WebBrowser-Steuerelement seinen Zustand wiederherstellen, einschließlich der Aufgabe, die richtigen Dokumente in Framesets zu laden.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Erstellen einer Internetverknüpfung über eine URL

Sie können auch eine Internetverknüpfung erstellen, wenn Sie über die URL der Seite verfügen, mit der Sie verknüpfen möchten.

1.  Erstellen Sie mit [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)eine Instanz des Internetverknüpfungsobjekts mithilfe einer CLSID von CLSID \_ InternetShortcut.
2.  Verwenden Sie die [IUniformResourceLocator::SetURL-Methode,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) um die URL in der Verknüpfung festzulegen.
3.  Verwenden Sie die [IPersistFile::Save-Methode,](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) um die Verknüpfungsdatei an einem gewünschten Speicherort zu speichern.

## <a name="accessing-property-storage"></a>Zugreifen auf eigenschaften Storage

Das Internetverknüpfungsobjekt enthält mehrere Eigenschaften, auf die Sie über die [IPropertySetStorage-Schnittstelle](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) des Objekts mit dem folgenden Verfahren zugreifen können.

1.  Rufen Sie die [IPropertySetStorage-Schnittstelle](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) ab, indem [Sie QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) mit IID \_ IPropertySetStorage aufrufen.
2.  Greifen Sie auf den Speicher für die Internetverknüpfungseigenschaft zu, indem [Sie IPropertySetStorage::Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) mit FMTID \_ Intshcut oder FMTID \_ InternetSite aufrufen, um die [IPropertyStorage-Schnittstelle](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) abzurufen.
3.  Lesen Sie die Eigenschaftenspeicherinformationen mit [IPropertyStorage::ReadMultiple,](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) indem Sie die entsprechende Eigenschaften-ID übergeben.

Mit [Version 4.70 oder höher](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) von Shell32.dll können Sie auch die [IPropertySetStorage-Schnittstelle](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) abrufen, indem Sie [**IShellFolder::BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) aufrufen, wobei der *pidl-Parameter* auf festgelegt ist. URL-Datei und der *riid-Parameter,* die auf IID \_ IPropertySetStorage festgelegt sind.

Die folgenden Eigenschaften-IDs können für FMTID \_ Intshcut angefordert werden.



| PROPID               | Variant-Typ | BESCHREIBUNG                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ IS \_ URL         | VT \_ LPWSTR   | URL, zu der die Verknüpfung führt             |
| PID \_ IS \_ NAME        | VT \_ LPWSTR   | Name der Internetverknüpfung               |
| PID \_ IS \_ WORKINGDIR  | VT \_ LPWSTR   | Arbeitsverzeichnis für die Verknüpfung          |
| PID \_ IST \_ HOTKEY      | VT \_ UI2      | Hotkey für die Verknüpfung                     |
| PID \_ IST \_ SHOWCMD     | VT \_ I4       | Befehl "Show" für Verknüpfung anzeigen                   |
| PID \_ IS \_ ICONINDEX   | VT \_ I4       | Index des Symbols                           |
| PID \_ IS \_ ICONFILE    | VT \_ LPWSTR   | Datei, die das Symbol enthält                 |
| PID \_ IS \_ WHATSNEW    | VT \_ LPWSTR   | What es New text (Neues in Text)                             |
| PID \_ IS \_ AUTHOR      | VT \_ LPWSTR   | Autor                                      |
| PID \_ IS \_ DESCRIPTION | VT \_ LPWSTR   | Beschreibungstext der Website                    |
| PID \_ IS \_ COMMENT     | VT \_ LPWSTR   | Kommentar mit Anmerkungen des Benutzers                      |
| PID \_ WIRD \_ ROAMED      | VT \_ BOOL     | True, wenn die Verknüpfung zum ersten Mal übertragen wird |



 

Die folgenden Eigenschaften-IDs können für FMTID InternetSite angefordert \_ werden.



| PROPID                     | Variant-Typ | BESCHREIBUNG                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ INTSITE \_ WHATSNEW     | VT \_ LPWSTR   | What es New text (Neues in Text)                                   |
| PID \_ INTSITE \_ AUTHOR       | VT \_ LPWSTR   | Autor                                            |
| PID \_ INTSITE \_ LASTVISIT    | VT \_ FILETIME | Zeitpunkt des letzten Besuchs der Website                        |
| PID \_ INTSITE \_ LASTMOD      | VT \_ FILETIME | Zeitpunkt der letzten Änderung des Standorts                       |
| PID \_ INTSITE \_ VISITCOUNT   | VT \_ UI4      | Anzahl der Benutzerbesuche                  |
| PID \_ INTSITE \_ DESCRIPTION  | VT \_ LPWSTR   | Beschreibungstext der Website                          |
| PID \_ INTSITE \_ COMMENT      | VT \_ LPWSTR   | Kommentar mit Anmerkung durch den Benutzer                            |
| \_PID-INTSITE-FLAGS \_        | VT \_ UI4      | Gibt die Verwendung von PIDISF-Flags \_ an (siehe unten).       |
| PID \_ INTSITE \_ CONTENTLEN   | Nicht zutreffend          | Derzeit nicht unterstützt                           |
| PID \_ INTSITE \_ CONTENTCODE  | Nicht zutreffend          | Derzeit nicht unterstützt                           |
| PID \_ INTSITE \_ RECURSE      | Nicht zutreffend          | Derzeit nicht unterstützt                           |
| PID \_ INTSITE \_ WATCH        | Nicht zutreffend          | Derzeit nicht unterstützt                           |
| PID \_ INTSITE-ABONNEMENT \_ | VT \_ UI8      | SUBSCRIPTIONCOOKIE-Wert für Abonnement-Manager |
| \_PID-INTSITE-URL \_          | VT \_ LPWSTR   | URL, zu der die Verknüpfung führt                   |
| PID \_ INTSITE \_ TITLE        | VT \_ LPWSTR   | Titel                                             |
| PID \_ INTSITE \_ CODEPAGE     | VT \_ UI4      | Codepage des Dokuments                          |
| \_PID-INTSITE-NACHVERFOLGUNG \_     | Nicht zutreffend          | Derzeit nicht unterstützt                           |
| PID \_ INTSITE \_ ICONINDEX    | VT \_ I4       | Index des Symbols                                 |
| PID \_ INTSITE \_ ICONFILE     | VT \_ LPWSTR   | Datei, die das Symbol enthält                       |
| PID \_ INTSITE \_ ROAMED       | VT \_ UI4      | Der Eintrag wurde aufgrund von Roaming hinzugefügt.                |



 

Im Folgenden finden Sie die Internetwebsiteflags.



| Flag                    | Beschreibung                                |
|-------------------------|--------------------------------------------|
| PIDISF \_ RECENTLYCHANGED | Gibt an, dass ein Standort vor Kurzem geändert wurde. |
| PIDISF \_ CACHEDSTICKY    | Derzeit nicht unterstützt                    |
| PIDISF \_ CACHEIMAGES     | Derzeit nicht unterstützt                    |
| PIDISF \_ FOLLOWALLLINKS  | Derzeit nicht unterstützt                    |



 

Die folgenden Werte werden für den Internetroamingverlauf verwendet.



| Wert von PID \_ INTSITE \_ ROAMED         | BESCHREIBUNG                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wert nicht festgelegt oder PIDISR \_ UP \_ TO \_ DATE | Dieser Cacheeintrag wurde durch das Roaming nicht geändert.                                                                                                                       |
| PIDISR \_ MUSS HINZUGEFÜGT \_ WERDEN                    | Dieser Cacheeintrag wurde dem Cache durch Roaming hinzugefügt. Legen Sie PIDISR \_ UP \_ TO DATE \_ fest, sobald die Verarbeitung des Eintrags abgeschlossen ist.                                                   |
| PIDISR \_ BENÖTIGT \_ UPDATE                 | Dieser Cacheeintrag war bereits auf dem lokalen Computer vorhanden, wurde jedoch durch das Roaming aktualisiert. Legen Sie PIDISR \_ UP \_ TO DATE \_ fest, sobald die Verarbeitung des Eintrags abgeschlossen ist.                 |
| PIDISR \_ MUSS GELÖSCHT \_ WERDEN                 | Roaming hat erkannt, dass dieser Cacheeintrag gelöscht werden soll. Beispielsweise kann der Benutzer seinen Browserverlauf gelöscht haben. Löschen Sie den Eintrag mit DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Schnittstellen

Das Internetverknüpfungsobjekt macht eine Reihe von Schnittstellen verfügbar.

### <a name="ole-interfaces"></a>OLE-Schnittstellen

-   [Idataobject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [Ipersistfile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [Ipersiststream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [Iolecommandtarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [Iobjectwithsite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Shellschnittstellen

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Funktionen

Es gibt mehrere Hilfsfunktionen, die mit dem Internetverknüpfungsobjekt verwendet werden können.

### <a name="internet-shortcut-utility-functions"></a>Funktionen des Internetverknüpfungs-Hilfsprogramms

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 
---
description: A Shell link is a data object that contains information used to access another object in the Shell's namespace&\#8212;that is, any object visible through Windows Explorer.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Shelllinks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f9f5e639cfa3619d5c79b011ab101af7c25ed1813db1c96b9f5422504f8c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859022"
---
# <a name="shell-links"></a>Shelllinks

A *Shell link* is a data object that contains information used to access another object in the Shell's namespace—that is, any object visible through Windows Explorer. Zu den Objekttypen, auf die über Shelllinks zugegriffen werden kann, gehören Dateien, Ordner, Laufwerke und Drucker. Mit einem Shelllink kann ein Benutzer oder eine Anwendung von überall im Namespace auf ein Objekt zugreifen. Der Benutzer oder die Anwendung muss den aktuellen Namen und Speicherort des Objekts nicht kennen.

-   [Informationen zu Shelllinks](#about-shell-links)
    -   [Linkauflösung](#link-resolution)
    -   [Verknüpfungsdateien](#link-files)
    -   [Elementbezeichner und Bezeichnerlisten](#item-identifiers-and-identifier-lists)
-   [Verwenden von Shelllinks](#using-shell-links)
    -   [Erstellen einer Verknüpfung und einer Ordnerverknüpfung zu einer Datei](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Auflösen einer Verknüpfung](#resolving-a-shortcut)
    -   [Erstellen einer Verknüpfung mit einem Nichtdateiobjekt](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>Informationen zu Shelllinks

Der Benutzer erstellt einen Shell-Link, indem er im Kontextmenü eines Objekts den Befehl Verknüpfung erstellen auswählt.  Das System erstellt automatisch ein Symbol für den Shell-Link, indem es das Symbol des Objekts mit einem kleinen Pfeil (auch bekannt als systemdefiniertes Linküberlagerungssymbol) kombiniert, der in der unteren linken Ecke des Symbols angezeigt wird. Ein Shelllink mit einem Symbol wird als Verknüpfung bezeichnet. Die Begriffe Shelllink und Verknüpfung werden jedoch häufig synonym verwendet. In der Regel erstellt der Benutzer Verknüpfungen, um schnellen Zugriff auf Objekte zu erhalten, die in Unterordnern oder freigegebenen Ordnern auf anderen Computern gespeichert sind. Beispielsweise kann ein Benutzer eine Verknüpfung zu einem Microsoft Word erstellen, das sich in einem Unterordner befindet, und das Verknüpfungssymbol auf dem Desktop platzieren. Der Benutzer kann dann das Dokument öffnen, indem er auf das Verknüpfungssymbol doppelklickt. Wenn das Dokument nach dem Erstellen der Verknüpfung verschoben oder umbenannt wird, versucht das System, die Verknüpfung zu aktualisieren, wenn der Benutzer sie das nächste Mal auswählt.

Anwendungen können auch Shelllinks und Verknüpfungen erstellen und verwenden. Beispielsweise könnte eine Anwendung für die Textverarbeitung einen Shell-Link erstellen, um eine Liste der zuletzt verwendeten Dokumente zu implementieren. Eine Anwendung erstellt einen Shell-Link mithilfe der [**IShellLink-Schnittstelle,**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) um ein Shell-Linkobjekt zu erstellen. Die Anwendung verwendet die [**IPersistFile-**](/windows/win32/api/objidl/nn-objidl-ipersistfile) oder [**IPersistStream-Schnittstelle,**](/windows/win32/api/objidl/nn-objidl-ipersiststream) um das Objekt in einer Datei oder einem Stream zu speichern.

> [!Note]  
> Sie können [**IShellLink nicht verwenden,**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) um einen Link zu einer URL zu erstellen.

 

In dieser Übersicht wird die [**IShellLink-Schnittstelle**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) beschrieben und erläutert, wie Sie damit Shelllinks in einer Microsoft Win32-basierten Anwendung erstellen und auflösen. Da der Entwurf von Shelllinks auf OLE Component Object Model (COM) basiert, sollten Sie mit den grundlegenden Konzepten der COM- und OLE-Programmierung vertraut sein, bevor Sie diese Übersicht lesen.

### <a name="link-resolution"></a>Linkauflösung

Wenn ein Benutzer eine Verknüpfung zu einem Objekt erstellt und der Name oder Speicherort des Objekts später geändert wird, führt das System automatisch Schritte aus, um die Verknüpfung zu aktualisieren oder aufzulösen, wenn der Benutzer sie das nächste Mal auswählt. Wenn eine Anwendung jedoch einen Shelllink erstellt und in einem Stream speichert, versucht das System nicht automatisch, den Link aufzulösen. Die Anwendung muss den Link auflösen, indem sie die [**IShellLink::Resolve-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) aufruft.

Wenn ein Shell-Link erstellt wird, speichert das System Informationen zum Link. Beim Auflösen eines Links – entweder automatisch oder mit einem [**IShellLink::Resolve-Aufruf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) – ruft das System zuerst den Pfad ab, der dem Shelllink zugeordnet ist, indem es einen Zeiger auf die Bezeichnerliste des Shelllinks verwendet. Weitere Informationen zur Bezeichnerliste finden Sie unter [Elementbezeichner und Bezeichnerlisten.](#item-identifiers-and-identifier-lists) Das System sucht in diesem Pfad nach dem zugeordneten Objekt und löst den Link auf, wenn es das Objekt findet. Wenn das System das Objekt nicht finden kann, ruft es den Dienst [Distributed Link Tracking and Object Identifiers](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT) auf, falls verfügbar, um das Objekt zu suchen. Wenn der DLT-Dienst nicht verfügbar ist oder das Objekt nicht finden kann, sucht das System im selben Verzeichnis nach einem Objekt mit der gleichen Dateierstellungszeit und denselben Attributen, aber mit einem anderen Namen. Dieser Suchtyp löst einen Link zu einem Objekt auf, das umbenannt wurde.

Wenn das System das Objekt immer noch nicht finden kann, durchsucht es die Verzeichnisse, den Desktop und die lokalen Volumes und sucht rekursiv durch die Verzeichnisstruktur nach einem Objekt mit demselben Namen oder der erstellungszeit. Wenn das System immer noch keine Übereinstimmung findet, wird ein Dialogfeld angezeigt, in dem der Benutzer zur Eingabe eines Speicherorts aufgefordert wird. Eine Anwendung kann das Dialogfeld unterdrücken, indem sie den **SLR \_ NO \_ UI-Wert** in einem Aufruf von [**IShellLink::Resolve ankündigt.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)

### <a name="initialization-of-the-component-object-library"></a>Initialisierung der Komponentenobjektbibliothek

Bevor eine Anwendung Verknüpfungen erstellen und auflösen kann, muss sie die Komponentenobjektbibliothek initialisieren, indem sie die [**CoInitialize-Funktion**](/windows/win32/api/objbase/nf-objbase-coinitialize) aufruft. Jeder Aufruf von **CoInitialize** erfordert einen entsprechenden Aufruf der [**CoUninitialize-Funktion,**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) die eine Anwendung aufrufen sollte, wenn sie beendet wird. Durch den Aufruf von **CoUninitialize** wird sichergestellt, dass die Anwendung erst beendet wird, wenn alle ausstehenden Nachrichten empfangen wurden.

### <a name="location-independent-names"></a>Location-Independent Namen

Das System stellt standortunabhängige Namen für Shelllinks zu Objekten in freigegebenen Ordnern zurVerfälsungen. Wenn das Objekt lokal gespeichert wird, stellt das System den lokalen Pfad und Dateinamen für das Objekt zurt. Wenn das Objekt remote gespeichert wird, stellt das System einen Universal Naming Convention Netzwerkressourcennamen (UNC) für das Objekt zur. Da das System standortunabhängige Namen bietet, kann ein Shelllink als universeller Name für eine Datei dienen, die auf andere Computer übertragen werden kann.

### <a name="link-files"></a>Verknüpfungsdateien

Wenn der Benutzer eine Verknüpfung zu einem  Objekt erstellt, indem er im Kontextmenü des Objekts den Befehl Verknüpfung erstellen auswählt, speichert Windows die Informationen, die er für den Zugriff auf das Objekt benötigt, in einer Linkdatei– einer Binärdatei mit der Dateierweiterung .lnk. Eine Linkdatei enthält die folgenden Informationen:

-   Der Speicherort (Pfad) des Objekts, auf das durch die Verknüpfung verwiesen wird (als entsprechendes Objekt bezeichnet).
-   Das Arbeitsverzeichnis des entsprechenden -Objekts.
-   Die Liste der Argumente, die das System an das entsprechende Objekt übergibt, wenn die [**IContextMenu::InvokeCommand-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) für die Verknüpfung aktiviert wird.
-   Der Show-Befehl, der verwendet wird, um den anfänglichen Show-Zustand des entsprechenden -Objekts fest zu legen. Dies ist einer der \_ SW-Werte, die in [**ShowWindow beschrieben werden.**](/windows/win32/api/winuser/nf-winuser-showwindow)
-   Der Speicherort (Pfad und Index) des Symbols der Verknüpfung.
-   Die Beschreibungszeichenfolge der Verknüpfung.
-   Die Tastenkombination für die Tastenkombination.

Wenn eine Linkdatei gelöscht wird, ist das entsprechende Objekt nicht betroffen.

Wenn Sie eine Verknüpfung zu einer anderen Verknüpfung erstellen, kopiert das System einfach die Linkdatei, anstatt eine neue Linkdatei zu erstellen. In diesem Fall sind die Verknüpfungen nicht voneinander unabhängig.

Eine Anwendung kann eine Dateinamenerweiterung als Verknüpfungsdateityp registrieren. Wenn eine Datei über eine Dateinamenerweiterung verfügt, die als Verknüpfungsdateityp registriert wurde, fügt das System dem Symbol der Datei automatisch das systemdefinierte Linküberlagerungssymbol (einen kleinen Pfeil) hinzu. Um eine Dateinamenerweiterung als Verknüpfungsdateityp zu registrieren, müssen Sie den IsShortcut-Wert der Registrierungsbeschreibung der Dateierweiterung hinzufügen, wie im folgenden Beispiel gezeigt. Beachten Sie, dass die Shell neu gestartet werden muss, damit das Überlagerungssymbol wirksam wird. IsShortcut hat keinen Datenwert.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Verknüpfungsnamen

Der Name der Verknüpfung, bei der es sich um eine Zeichenfolge handelt, die unterhalb des Shell-Linksymbols angezeigt wird, ist tatsächlich der Dateiname der Verknüpfung selbst. Der Benutzer kann die Beschreibungszeichenfolge bearbeiten, indem er sie auswählt und eine neue Zeichenfolge eingibt.

### <a name="location-of-shortcuts-in-the-namespace"></a>Speicherort der Verknüpfungen im Namespace

Eine Verknüpfung kann auf dem Desktop oder an einer beliebigen Stelle im Namespace der Shell vorhanden sein. Ebenso kann das -Objekt, das der Verknüpfung zugeordnet ist, auch an einer beliebigen Stelle im Namespace der Shell vorhanden sein. Eine Anwendung kann die [**IShellLink::SetPath-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) verwenden, um den Pfad und Dateinamen für das zugeordnete Objekt und die [**IShellLink::GetPath-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) zum Abrufen des aktuellen Pfads und Dateinamens für das Objekt zu verwenden.

### <a name="shortcut-working-directory"></a>Verknüpfungsarbeitsverzeichnis

Das Arbeitsverzeichnis ist das Verzeichnis, in dem das entsprechende Objekt einer Verknüpfung Dateien lädt oder speichert, wenn der Benutzer kein bestimmtes Verzeichnis identifiziert. Eine Linkdatei enthält den Namen des Arbeitsverzeichnisses für das entsprechende Objekt. Eine Anwendung kann den Namen des Arbeitsverzeichnisses für das entsprechende Objekt mithilfe der [**IShellLink::SetWorkingDirectory-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) festlegen und den Namen des aktuellen Arbeitsverzeichnisses für das entsprechende Objekt mithilfe der [**IShellLink::GetWorkingDirectory-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) abrufen.

### <a name="shortcut-command-line-arguments"></a>Verknüpfungsbefehlszeilenargumente

Eine Linkdatei enthält Befehlszeilenargumente, die die Shell an das entsprechende Objekt übergibt, wenn der Benutzer den Link auswählt. Eine Anwendung kann die Befehlszeilenargumente für eine Verknüpfung mithilfe der [**IShellLink::SetArguments-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) festlegen. Es ist hilfreich, Befehlszeilenargumente zu setzen, wenn die entsprechende Anwendung, z. B. ein Linker oder Compiler, spezielle Flags als Argumente an nimmt. Eine Anwendung kann die Befehlszeilenargumente mithilfe der [**IShellLink::GetArguments-Methode**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) aus einer Verknüpfung abrufen.

### <a name="shortcut-show-commands"></a>Befehle zum Anzeigen von Verknüpfungen

Wenn der Benutzer auf eine Verknüpfung doppelklickt, startet das System die Anwendung, die dem entsprechenden -Objekt zugeordnet ist, und legt den anfänglichen Showzustand der Anwendung basierend auf dem durch die Verknüpfung angegebenen Show-Befehl fest. Der Befehl show kann einer der \_ SW-Werte sein, die in der Beschreibung der [**ShowWindow-Funktion enthalten**](/windows/win32/api/winuser/nf-winuser-showwindow) sind. Eine Anwendung kann den Befehl show für eine Verknüpfung mithilfe der [**IShellLink::SetShowCmd-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) festlegen und den aktuellen show-Befehl mithilfe der [**IShellLink::GetShowCmd-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) abrufen.

### <a name="shortcut-icons"></a>Verknüpfungssymbole

Wie bei anderen Shellobjekten verfügt auch eine Verknüpfung über ein Symbol. Der Benutzer greifen auf das -Objekt zu, das einer Verknüpfung zugeordnet ist, indem er auf das Symbol der Verknüpfung doppelklickt. Wenn das System ein Symbol für eine Verknüpfung erstellt, verwendet es die Bitmap des entsprechenden Objekts und fügt das systemdefinierte Linküberlagerungssymbol (einen kleinen Pfeil) der unteren linken Ecke hinzu. Eine Anwendung kann den Speicherort (Pfad und Index) des Symbols einer Verknüpfung mithilfe der [**IShellLink::SetIconLocation-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) festlegen. Eine Anwendung kann diesen Speicherort mithilfe der [**IShellLink::GetIconLocation-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) abrufen.

### <a name="shortcut-descriptions"></a>Beschreibungen von Verknüpfungen

Verknüpfungen enthalten Beschreibungen, die dem Benutzer jedoch nie angezeigt werden. Eine Anwendung kann eine Beschreibung verwenden, um beliebige Textinformationen zu speichern. Beschreibungen werden mithilfe der [**IShellLink::SetDescription-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) festgelegt und mithilfe der [**IShellLink::GetDescription-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) abgerufen.

### <a name="shortcut-keyboard-shortcuts"></a>Tastenkombinationen

Einem Verknüpfungsobjekt kann eine Tastenkombination zugeordnet sein. Mit Tastenkombinationen kann ein Benutzer eine Tastenkombination drücken, um eine Tastenkombination zu aktivieren. Eine Anwendung kann die Tastenkombination für eine Verknüpfung mithilfe der [**IShellLink::SetHotkey-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) festlegen und die aktuelle Tastenkombination mithilfe der [**IShellLink::GetHotkey-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) abrufen.

### <a name="item-identifiers-and-identifier-lists"></a>Elementbezeichner und Bezeichnerlisten

Die Shell verwendet Objektbezeichner innerhalb des Namespace der Shell. Alle in der Shell sichtbaren Objekte (Dateien, Verzeichnisse, Server, Arbeitsgruppen usw.) verfügen über eindeutige Bezeichner zwischen den Objekten innerhalb ihres übergeordneten Ordners. Diese Bezeichner werden als Elementbezeichner bezeichnet und weisen den [**SHITEMID-Datentyp**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) auf, wie in der Headerdatei Shtypes.h definiert. Ein Elementbezeichner ist ein Bytestream variabler Länge, der Informationen enthält, die ein Objekt innerhalb eines Ordners identifizieren. Nur der Ersteller eines Elementbezeichners kennt den Inhalt und das Format des Bezeichners. Der einzige Teil eines Elementbezeichners, der von der Shell verwendet wird, sind die ersten beiden Bytes, die die Größe des Bezeichners angeben.

Jeder übergeordnete Ordner verfügt über einen eigenen Elementbezeichner, der ihn innerhalb seines eigenen übergeordneten Ordners identifiziert. Daher kann jedes Shellobjekt durch eine Liste von Elementbezeichnern eindeutig identifiziert werden. Ein übergeordneter Ordner speichert eine Liste von Bezeichnern für die darin enthaltenen Elemente. Die Liste weist den [**ITEMIDLIST-Datentyp**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) auf. Elementbezeichnerlisten werden von der Shell zugeordnet und können über Shellschnittstellen wie [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)übergeben werden. Beachten Sie, dass jeder Bezeichner in einer Elementbezeichnerliste nur innerhalb des Kontexts des übergeordneten Ordners sinnvoll ist.

Eine Anwendung kann die Elementbezeichnerliste einer Verknüpfung mithilfe der [**IShellLink::SetIDList-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) festlegen. Diese Methode ist nützlich, wenn Sie eine Verknüpfung auf ein Objekt festlegen, das keine Datei ist, z. B. einen Drucker oder ein Laufwerk. Eine Anwendung kann die Elementbezeichnerliste einer Verknüpfung mithilfe der [**IShellLink::GetIDList-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) abrufen.

## <a name="using-shell-links"></a>Verwenden von Shelllinks

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Verknüpfungen innerhalb einer Win32-basierten Anwendung erstellt und aufgelöst werden. In diesem Abschnitt wird davon ausgegangen, dass Sie mit der Win32-, C++- und OLE COM-Programmierung vertraut sind.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Erstellen einer Verknüpfung und einer Ordnerverknüpfung zu einer Datei

Die CreateLink-Beispielfunktion im folgenden Beispiel erstellt eine Verknüpfung. Die Parameter enthalten einen Zeiger auf den Namen der Datei, mit der eine Verknüpfung erstellt werden soll, einen Zeiger auf den Namen der verknüpfung, die Sie erstellen, und einen Zeiger auf die Beschreibung des Links. Die Beschreibung besteht aus der Zeichenfolge "Shortcut to **file name",** wobei **dateiname** der Name der Datei ist, mit der verknüpft werden soll.

Um eine Ordnerverknüpfung mithilfe der CreateLink-Beispielfunktion zu erstellen, rufen Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit CLSID \_ FolderShortcut anstelle von CLSID \_ ShellLink auf (CLSID \_ FolderShortcut unterstützt IShellLink). Der gesamte andere Code bleibt unverändert.

Da CreateLink die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufruft, wird davon ausgegangen, dass die [**CoInitialize-Funktion**](/windows/win32/api/objbase/nf-objbase-coinitialize) bereits aufgerufen wurde. CreateLink verwendet die [**IPersistFile-Schnittstelle,**](/windows/win32/api/objidl/nn-objidl-ipersistfile) um die Verknüpfung zu speichern, und die [**IShellLink-Schnittstelle**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) zum Speichern des Dateinamens und der Beschreibung.


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>Auflösen einer Verknüpfung

Eine Anwendung muss möglicherweise auf eine verknüpfung zugreifen und diese bearbeiten, die zuvor erstellt wurde. Dieser Vorgang wird als Auflösen der Verknüpfung bezeichnet.

Die anwendungsdefinierte ResolveIt-Funktion im folgenden Beispiel löst eine Verknüpfung auf. Zu den Parametern gehören ein Fensterhandle, ein Zeiger auf den Pfad der Verknüpfung und die Adresse eines Puffers, der den neuen Pfad zum Objekt empfängt. Das Fensterhandle identifiziert das übergeordnete Fenster für alle Meldungsfelder, die die Shell möglicherweise anzeigen muss. Beispielsweise kann die Shell ein Meldungsfeld anzeigen, wenn sich der Link auf nicht verfügbaren Medien befindet, wenn Netzwerkprobleme auftreten, wenn der Benutzer eine Diskette einfügen muss usw.

Die ResolveIt-Funktion ruft die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf und geht davon aus, dass die [**CoInitialize-Funktion**](/windows/win32/api/objbase/nf-objbase-coinitialize) bereits aufgerufen wurde. Beachten Sie, dass ResolveIt die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) verwenden muss, um die Linkinformationen zu speichern. **IPersistFile** wird vom [**IShellLink-Objekt**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) implementiert. Die Linkinformationen müssen geladen werden, bevor die Pfadinformationen abgerufen werden. Dies wird später im Beispiel gezeigt. Wenn die Linkinformationen nicht geladen werden, schlagen die Aufrufe der [**IShellLink::GetPath-**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) und [**IShellLink::GetDescription-Memberfunktionen**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) fehl.


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Erstellen einer Verknüpfung mit einem Nichtdateiobjekt

Das Erstellen einer Verknüpfung mit einem Nichtdateiobjekt, z. B. einem Drucker, ähnelt dem Erstellen einer Verknüpfung mit einer Datei, außer dass Sie die Bezeichnerliste auf den Drucker festlegen müssen, anstatt den Pfad zur Datei festzulegen. Um die Bezeichnerliste festzulegen, rufen Sie die [**IShellLink::SetIDList-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) auf und geben die Adresse einer Bezeichnerliste an.

Jedes Objekt im Namespace der Shell verfügt über einen Elementbezeichner. Die Shell verkettet Elementbezeichner häufig in Listen mit NULL-Terminierung, die aus einer beliebigen Anzahl von Elementbezeichnern bestehen. Weitere Informationen zu Elementbezeichnern finden Sie unter [Elementbezeichner und Bezeichnerlisten.](#item-identifiers-and-identifier-lists)

Im Allgemeinen verfügen Sie bereits über einen Zeiger auf die [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Objekts, wenn Sie eine Verknüpfung auf ein Element festlegen müssen, das keinen Dateinamen hat, z. B. einen Drucker. **IShellFolder** wird verwendet, um Namespaceerweiterungen zu erstellen.

Sobald Sie über den Klassenbezeichner für [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)verfügen, können Sie die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um die Adresse der Schnittstelle abzurufen. Anschließend können Sie die -Schnittstelle aufrufen, um die Objekte im Ordner aufzuzählen und die Adresse des Elementbezeichners für das gesuchte Objekt abzurufen. Schließlich können Sie die Adresse in einem Aufruf der [**IShellLink::SetIDList-Memberfunktion**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) verwenden, um eine Verknüpfung mit dem Objekt zu erstellen.

 

 

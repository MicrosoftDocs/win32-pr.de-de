---
description: Ein shelllink ist ein Datenobjekt, das Informationen enthält, die für den Zugriff auf ein anderes Objekt im Namespace der Shell&8212 verwendet werden, d \# . h. alle Objekte, die über Windows Explorer sichtbar sind.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Shelllinks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216610"
---
# <a name="shell-links"></a>Shelllinks

Ein *shelllink* ist ein Datenobjekt, das Informationen enthält, die für den Zugriff auf ein anderes Objekt im-Namespace der Shell verwendet werden, d. –. alle Objekte, die über Windows Explorer sichtbar sind. Zu den Typen von Objekten, auf die über Shellverknüpfungen zugegriffen werden kann, gehören Dateien, Ordner, Laufwerke und Drucker. Ein shelllink ermöglicht einem Benutzer oder einer Anwendung den Zugriff auf ein Objekt von einer beliebigen Stelle im Namespace aus. Der Benutzer oder die Anwendung muss den aktuellen Namen und Speicherort des Objekts nicht kennen.

-   [Informationen zu shelllinks](#about-shell-links)
    -   [Link Auflösung](#link-resolution)
    -   [Dateien verknüpfen](#link-files)
    -   [Element Bezeichner und bezeichnerlisten](#item-identifiers-and-identifier-lists)
-   [Verwenden von shelllinks](#using-shell-links)
    -   [Erstellen einer Verknüpfung und einer Ordner Verknüpfung zu einer Datei](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Auflösen einer Verknüpfung](#resolving-a-shortcut)
    -   [Erstellen einer Verknüpfung mit einem nicht Datei Objekt](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>Informationen zu shelllinks

Der Benutzer erstellt eine Shellverknüpfung, indem er im Kontextmenü eines Objekts den Befehl **Verknüpfung erstellen** auswählt. Das System erstellt automatisch ein Symbol für die Shellverknüpfung, indem das Symbol des Objekts mit einem kleinen Pfeil (als System definiertes Link Überlagerungs Symbol bezeichnet) kombiniert wird, das in der unteren linken Ecke des Symbols angezeigt wird. Ein shelllink mit einem Symbol wird als Verknüpfung bezeichnet. die Begriffe "shelllink" und "Verknüpfung" werden jedoch häufig austauschbar verwendet. In der Regel erstellt der Benutzer Verknüpfungen, um schnellen Zugriff auf Objekte zu erhalten, die in Unterordnern oder in freigegebenen Ordnern auf anderen Computern gespeichert sind. Beispielsweise kann ein Benutzer eine Verknüpfung mit einem Microsoft Word-Dokument erstellen, das sich in einem Unterordner befindet, und das Verknüpfungs Symbol auf dem Desktop platzieren. Der Benutzer kann dann das Dokument öffnen, indem er auf das Verknüpfungs Symbol doppelklickt. Wenn das Dokument nach dem Erstellen der Verknüpfung verschoben oder umbenannt wird, versucht das System, die Verknüpfung zu aktualisieren, wenn der Benutzer das nächste Mal auswählt.

Anwendungen können auch shelllinks und Verknüpfungen erstellen und verwenden. Beispielsweise kann eine Textverarbeitungsanwendung einen shelllink erstellen, um eine Liste der zuletzt verwendeten Dokumente zu implementieren. Eine Anwendung erstellt eine Shellverknüpfung, indem Sie die [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle zum Erstellen eines shelllinkobjekts verwendet. Die Anwendung verwendet die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -oder [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle, um das Objekt in einer Datei oder einem Stream zu speichern.

> [!Note]  
> Sie können [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) nicht verwenden, um einen Link zu einer URL zu erstellen.

 

In dieser Übersicht wird die [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle beschrieben und erläutert, wie Sie Sie zum Erstellen und Auflösen von Shellverknüpfungen in einer Microsoft Win32-basierten Anwendung verwenden können. Da der Entwurf von shelllinks auf der OLE-Component Object Model (com) basiert, sollten Sie sich mit den grundlegenden Konzepten der com-und OLE-Programmierung vertraut machen, bevor Sie diese Übersicht lesen.

### <a name="link-resolution"></a>Link Auflösung

Wenn ein Benutzer eine Verknüpfung zu einem Objekt erstellt und der Name oder Speicherort des Objekts zu einem späteren Zeitpunkt geändert wird, führt das System automatisch Schritte aus, um die Verknüpfung zu aktualisieren oder aufzulösen, wenn der Benutzer das nächste Mal auswählt. Wenn eine Anwendung jedoch einen shelllink erstellt und in einem Stream speichert, versucht das System nicht automatisch, den Link aufzulösen. Die Anwendung muss den Link auflösen, indem Sie die [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) -Methode aufrufen.

Wenn ein shelllink erstellt wird, speichert das Systeminformationen über den Link. Beim Auflösen eines Links – entweder automatisch oder mit einem [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) -Befehl, ruft das System zuerst den dem shelllink zugeordneten Pfad ab, indem er einen Zeiger auf die bezeichnerliste des shelllinks verwendet. Weitere Informationen zur bezeichnerliste finden Sie unter [Element Bezeichner und bezeichnerlisten](#item-identifiers-and-identifier-lists). Das System sucht in diesem Pfad nach dem zugeordneten Objekt und löst den Link auf, wenn das Objekt gefunden wird. Wenn das System das Objekt nicht finden kann, ruft es auf der [verteilten Link Verfolgung und](../fileio/distributed-link-tracking-and-object-identifiers.md) dem DLT-Dienst (Object Identifier, Objekt Bezeichner) auf, um das Objekt zu suchen. Wenn der DLT-Dienst nicht verfügbar ist oder das Objekt nicht finden kann, sucht das System im gleichen Verzeichnis nach einem Objekt mit derselben Datei Erstellungszeit und Attributen, aber mit einem anderen Namen. Bei dieser Art von Suche wird ein Link zu einem Objekt aufgelöst, das umbenannt wurde.

Wenn das System das Objekt immer noch nicht finden kann, durchsucht es die Verzeichnisse, den Desktop und die lokalen Volumes und sucht rekursiv nach der Verzeichnisstruktur für ein Objekt mit dem gleichen Namen oder der Erstellungszeit. Wenn das System immer noch keine Entsprechung findet, wird ein Dialogfeld angezeigt, in dem der Benutzer zur Eingabe eines Orts aufgefordert wird. Eine Anwendung kann das Dialogfeld unterdrücken, indem Sie den Wert der **\_ \_ Benutzeroberfläche ohne Benutzeroberfläche** in einem [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)-Rückruf angibt.

### <a name="initialization-of-the-component-object-library"></a>Initialisierung der Komponenten Objektbibliothek

Bevor eine Anwendung Verknüpfungen erstellen und auflösen kann, muss Sie die Komponenten Objektbibliothek initialisieren, indem Sie die [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) -Funktion aufrufen. Jeder **CoInitialize** -Rückruf erfordert einen entsprechenden-Rückruf für die Funktion " [**count**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) ", der von einer Anwendung beim Beenden aufgerufen werden soll. Der **CallInitialize** -Befehl stellt sicher, dass die Anwendung nicht beendet wird, bis Sie alle ausstehenden Nachrichten empfangen hat.

### <a name="location-independent-names"></a>Location-Independent Namen

Das System stellt standortunabhängige Namen für shelllinks zu Objekten bereit, die in freigegebenen Ordnern gespeichert sind. Wenn das-Objekt lokal gespeichert wird, stellt das System den lokalen Pfad und den Dateinamen für das-Objekt bereit. Wenn das-Objekt remote gespeichert wird, stellt das System einen Universal Naming Convention (UNC)-Netzwerkressourcen Namen für das-Objekt bereit. Da das Systemstandort unabhängige Namen bereitstellt, kann ein shelllink als universeller Name für eine Datei dienen, die auf andere Computer übertragen werden kann.

### <a name="link-files"></a>Dateien verknüpfen

Wenn der Benutzer eine Verknüpfung zu einem Objekt erstellt, indem er im Kontextmenü des Objekts den Befehl **Verknüpfung erstellen** auswählt, speichert Windows die Informationen, die er benötigt, um auf das Objekt in einer Linkdatei zuzugreifen – eine Binärdatei mit der Dateinamenerweiterung. lnk. Eine Linkdatei enthält die folgenden Informationen:

-   Der Speicherort (Pfad) des Objekts, auf das durch die Verknüpfung verwiesen wird (als entsprechendes Objekt bezeichnet).
-   Das Arbeitsverzeichnis des entsprechenden Objekts.
-   Die Liste der Argumente, die das System an das entsprechende Objekt übergibt, wenn die [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) -Methode für die Verknüpfung aktiviert wird.
-   Der Show-Befehl, der verwendet wird, um den anfänglichen Anzeige Zustand des entsprechenden Objekts festzulegen. Dies ist einer der \_ in [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)beschriebenen SW-Werte.
-   Der Speicherort (Pfad und Index) des Symbol der Verknüpfung.
-   Die Beschreibungs Zeichenfolge der Verknüpfung.
-   Die Tastenkombination für die Verknüpfung.

Wenn eine Linkdatei gelöscht wird, ist das entsprechende Objekt nicht betroffen.

Wenn Sie eine Verknüpfung zu einer anderen Verknüpfung erstellen, kopiert das System einfach die Linkdatei, anstatt eine neue Linkdatei zu erstellen. In diesem Fall sind die Verknüpfungen nicht unabhängig voneinander.

Eine Anwendung kann eine Dateinamenerweiterung als Dateityp für die Verknüpfung registrieren. Wenn eine Datei eine Dateinamenerweiterung hat, die als Verknüpfungs Dateityp registriert wurde, fügt das System automatisch das System definierte Link Überlagerungs Symbol (ein kleiner Pfeil) zum Symbol der Datei hinzu. Wenn Sie eine Dateinamenerweiterung als Verknüpfungs Dateityp registrieren möchten, müssen Sie den Wert IsShortcut der Registrierungs Beschreibung der Dateinamenerweiterung hinzufügen, wie im folgenden Beispiel gezeigt. Beachten Sie, dass die Shell neu gestartet werden muss, damit das Überlagerungs Symbol wirksam wird. IsShortcut hat keinen Datenwert.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Verknüpfungs Namen

Der Name der Verknüpfung, bei der es sich um eine Zeichenfolge handelt, die unterhalb des shelllinksymbols angezeigt wird, ist tatsächlich der Dateiname der Verknüpfung. Der Benutzer kann die Beschreibungs Zeichenfolge bearbeiten, indem er Sie auswählen und eine neue Zeichenfolge eingeben.

### <a name="location-of-shortcuts-in-the-namespace"></a>Speicherort von Verknüpfungen im Namespace

Eine Verknüpfung kann auf dem Desktop oder an einer beliebigen Stelle im-Namespace der Shell vorhanden sein. Ebenso kann das Objekt, das der Verknüpfung zugeordnet ist, auch an beliebiger Stelle im-Namespace der Shell vorhanden sein. Eine Anwendung kann die [**IShellLink:: setpath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) -Methode verwenden, um den Pfad und den Dateinamen für das zugeordnete Objekt festzulegen, und die [**IShellLink:: getpath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) -Methode, um den aktuellen Pfad und den Dateinamen für das Objekt abzurufen.

### <a name="shortcut-working-directory"></a>Arbeitsverzeichnis für die Verknüpfung

Das Arbeitsverzeichnis ist das Verzeichnis, in dem das entsprechende Objekt einer Verknüpfung Dateien lädt oder speichert, wenn der Benutzer kein bestimmtes Verzeichnis identifiziert. Eine Linkdatei enthält den Namen des Arbeitsverzeichnisses für das entsprechende Objekt. Eine Anwendung kann den Namen des Arbeitsverzeichnisses für das entsprechende Objekt mithilfe der [**IShellLink:: setworkingdirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) -Methode festlegen und den Namen des aktuellen Arbeitsverzeichnisses für das entsprechende Objekt mithilfe der [**IShellLink:: GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) -Methode abrufen.

### <a name="shortcut-command-line-arguments"></a>Befehlszeilenargumente für die Verknüpfung

Eine Linkdatei enthält Befehlszeilenargumente, die die Shell an das entsprechende Objekt übergibt, wenn der Benutzer den Link auswählt. Eine Anwendung kann die Befehlszeilenargumente für eine Verknüpfung mithilfe der [**IShellLink:: setArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) -Methode festlegen. Es ist hilfreich, Befehlszeilenargumente festzulegen, wenn die entsprechende Anwendung, z. b. ein linker oder ein Compiler, spezielle Flags als Argumente annimmt. Eine Anwendung kann die Befehlszeilenargumente mithilfe der [**IShellLink:: GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) -Methode aus einer Verknüpfung abrufen.

### <a name="shortcut-show-commands"></a>Tastenkombinationen anzeigen

Wenn der Benutzer auf eine Verknüpfung doppelklickt, startet das System die Anwendung, die dem entsprechenden Objekt zugeordnet ist, und legt den anfänglichen Ansichts Zustand der Anwendung auf der Grundlage des durch die Verknüpfung angegebenen Befehls anzeigen fest. Der Show-Befehl kann einer der \_ in der Beschreibung der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion enthaltenen SW-Werte sein. Eine Anwendung kann den Show-Befehl für eine Verknüpfung mithilfe der [**IShellLink:: setshowcmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) -Methode festlegen und kann den aktuellen Show-Befehl mithilfe der [**IShellLink:: getshowcmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) -Methode abrufen.

### <a name="shortcut-icons"></a>Tastenkombinationen

Wie bei anderen shellobjekten weist eine Verknüpfung ein Symbol auf. Der Benutzer greift auf das-Objekt zu, das einer Verknüpfung zugeordnet ist, indem er auf das Symbol der Verknüpfung doppelklickt. Wenn das System ein Symbol für eine Verknüpfung erstellt, wird die Bitmap des entsprechenden Objekts verwendet, und das System definierte linküberlagerungs Symbol (ein kleiner Pfeil) wird in der unteren linken Ecke hinzugefügt. Eine Anwendung kann den Speicherort (Pfad und Index) des Symbols einer Verknüpfung mithilfe der [**IShellLink:: setikonlocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) -Methode festlegen. Eine Anwendung kann diesen Speicherort mithilfe der [**IShellLink:: getikonlocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) -Methode abrufen.

### <a name="shortcut-descriptions"></a>Verknüpfungs Beschreibungen

Verknüpfungen verfügen über Beschreibungen, aber der Benutzer sieht diese nicht. Eine Anwendung kann eine Beschreibung verwenden, um Textinformationen zu speichern. Beschreibungen werden mithilfe der [**IShellLink:: setDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) -Methode festgelegt und mithilfe der [**IShellLink:: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) -Methode abgerufen.

### <a name="shortcut-keyboard-shortcuts"></a>Tastenkombinationen für Tastenkombinationen

Einem Verknüpfungs Objekt kann eine Tastenkombination zugeordnet werden. Tastenkombinationen ermöglichen Benutzern das Drücken einer Tastenkombination, um eine Verknüpfung zu aktivieren. Eine Anwendung kann die Tastenkombination für eine Verknüpfung mithilfe der [**IShellLink:: SetHotKey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) -Methode festlegen und die aktuelle Tastenkombination mithilfe der [**IShellLink:: GetHotKey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) -Methode abrufen.

### <a name="item-identifiers-and-identifier-lists"></a>Element Bezeichner und bezeichnerlisten

Die Shell verwendet Objekt Bezeichner im-Namespace der Shell. Alle Objekte, die in der Shell (Dateien, Verzeichnisse, Server, Arbeitsgruppen usw.) sichtbar sind, verfügen über eindeutige IDs zwischen den Objekten innerhalb ihres übergeordneten Ordners. Diese Bezeichner werden als Element Bezeichner bezeichnet und verfügen über den [**shitemid**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) -Datentyp, der in der Header Datei "shtypes. h" definiert ist. Ein Element Bezeichner ist ein Bytestream variabler Länge, der Informationen enthält, die ein Objekt in einem Ordner identifizieren. Nur der Ersteller eines Element Bezeichners kennt den Inhalt und das Format des Bezeichners. Der einzige Teil eines Element Bezeichners, der von der Shell verwendet wird, sind die ersten zwei Bytes, die die Größe des Bezeichners angeben.

Jeder übergeordnete Ordner verfügt über einen eigenen Element Bezeichner, der ihn innerhalb seines eigenen übergeordneten Ordners identifiziert. Folglich kann jedes Shellobjekt durch eine Liste von Element Bezeichner eindeutig identifiziert werden. Ein übergeordneter Ordner speichert eine Liste der Bezeichner für die darin enthaltenen Elemente. Die Liste enthält den [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Datentyp. Elementbezeichnerlisten werden von der Shell zugeordnet und können über Shellschnittstellen, wie z. b. [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), übermittelt werden. Beachten Sie, dass jeder Bezeichner in der Liste der Element Bezeichner nur innerhalb des Kontexts seines übergeordneten Ordners sinnvoll ist.

Eine Anwendung kann die elementbezeichnerliste einer Verknüpfung mithilfe der [**IShellLink:: setidlist**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) -Methode festlegen. Diese Methode ist nützlich, wenn Sie eine Verknüpfung zu einem Objekt festlegen, das keine Datei ist, z. b. ein Drucker oder ein Laufwerk. Eine Anwendung kann die elementbezeichnerliste eines Verknüpfungs Elements mithilfe der [**IShellLink:: getidlist**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) -Methode abrufen.

## <a name="using-shell-links"></a>Verwenden von shelllinks

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Verknüpfungen in einer Win32-basierten Anwendung erstellt und aufgelöst werden. In diesem Abschnitt wird davon ausgegangen, dass Sie mit der Programmierung von Win32, C++ und OLE COM vertraut sind.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Erstellen einer Verknüpfung und einer Ordner Verknüpfung zu einer Datei

Mit der Funktion "Beispiel Funktion" im folgenden Beispiel wird eine Verknüpfung erstellt. Die Parameter enthalten einen Zeiger auf den Namen der Datei, mit der eine Verknüpfung hergestellt werden soll, einen Zeiger auf den Namen der zu erstellenden Verknüpfung und einen Zeiger auf die Beschreibung des Links. Die Beschreibung besteht aus der Zeichenfolge "Verknüpfung mit **Dateiname**", wobei " **Dateiname** " der Name der Datei ist, mit der eine Verknüpfung hergestellt werden soll.

Rufen Sie zum Erstellen einer Ordner Verknüpfung mithilfe der Funktion "samatelink Sample" [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mithilfe \_ von CLSID foldershortcut auf, anstelle von CLSID \_ shelllink (CLSID \_ foldershortcut unterstützt IShellLink). Der gesamte andere Code bleibt unverändert.

Da die [**CoInitialize**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion von "aliatelink" aufgerufen wird, wird davon ausgegangen, dass die [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) -Funktion bereits aufgerufen wurde. "Kreatelink" verwendet die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle zum Speichern der Verknüpfung und die [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle zum Speichern des Datei namens und der Beschreibung.


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

Eine Anwendung muss möglicherweise auf eine zuvor erstellte Verknüpfung zugreifen und diese bearbeiten. Dieser Vorgang wird als Auflösen der Verknüpfung bezeichnet.

Durch die Anwendungs definierte resolveit-Funktion im folgenden Beispiel wird eine Verknüpfung aufgelöst. Zu den Parametern gehören ein Fenster Handle, ein Zeiger auf den Pfad der Verknüpfung und die Adresse eines Puffers, der den neuen Pfad zum Objekt empfängt. Das Fenster Handle identifiziert das übergeordnete Fenster für alle Meldungs Felder, die die Shell möglicherweise anzeigen muss. Beispielsweise kann die Shell ein Meldungs Feld anzeigen, wenn sich der Link auf nicht freigegebenen Medien befindet, wenn Netzwerkprobleme auftreten, wenn der Benutzer eine Diskette einfügen muss usw.

Die resolveit-Funktion Ruft die [**cokreatanstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf und geht davon aus, dass die [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) -Funktion bereits aufgerufen wurde. Beachten Sie, dass resolveit die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle zum Speichern der Link Informationen verwenden muss. **IPersistFile** wird durch das [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Objekt implementiert. Die Link Informationen müssen geladen werden, bevor die Pfadinformationen abgerufen werden. Dies wird später im Beispiel dargestellt. Wenn beim Laden der Link Informationen ein Fehler auftritt, werden die Aufrufe der Member-Funktionen [**IShellLink:: getpath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) und [**IShellLink:: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) fehlschlagen.


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



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Erstellen einer Verknüpfung mit einem nicht Datei Objekt

Das Erstellen einer Verknüpfung mit einem nicht Datei Objekt, wie z. b. einem Drucker, ähnelt dem Erstellen einer Verknüpfung zu einer Datei mit der Ausnahme, dass Sie die bezeichnerliste auf den Drucker festlegen müssen, anstatt den Pfad für die Datei festzulegen. Um die bezeichnerliste festzulegen, wenden Sie die [**IShellLink:: setidlist**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) -Methode an, und geben Sie dabei die Adresse einer bezeichnerliste an.

Jedes-Objekt im-Namespace der Shell hat einen Element Bezeichner. Die Shell verkettet häufig Element Bezeichner in mit NULL endenden Listen, die aus einer beliebigen Anzahl von Element bezeichaten bestehen. Weitere Informationen zu Element Bezeichnern finden Sie unter [Element Bezeichner und bezeichnerlisten](#item-identifiers-and-identifier-lists).

Wenn Sie eine Verknüpfung zu einem Element festlegen müssen, das keinen Dateinamen hat (z. b. ein Drucker), verfügen Sie im allgemeinen bereits über einen Zeiger auf die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Objekts. **IShellFolder** wird zum Erstellen von Namespace Erweiterungen verwendet.

Sobald Sie den Klassen Bezeichner für [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)haben, können Sie die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen, um die Adresse der Schnittstelle abzurufen. Anschließend können Sie die-Schnittstelle aufrufen, um die Objekte im Ordner aufzuzählen und die Adresse des Element Bezeichners für das gesuchte Objekt abzurufen. Schließlich können Sie die Adresse in einem Aufrufe der [**IShellLink:: setidlist**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) -Member-Funktion verwenden, um eine Verknüpfung mit dem-Objekt zu erstellen.

 

 

---
title: Verwenden des aktiven Desktop Objekts
description: Dieser Artikel enthält Informationen zum activedesktop-Objekt, das Teil der Windows-Shell-API ist. Mit diesem Objekt können Sie über die iactivedesktop-Schnittstelle Elemente auf dem Desktop hinzufügen, entfernen und ändern.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Activedesktop-Objekt
- Aktiver Desktop
- Enumeration, Desktop Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472805"
---
# <a name="using-the-active-desktop-object"></a>Verwenden des aktiven Desktop Objekts

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. \]

Dieser Artikel enthält Informationen zum **activedesktop-** Objekt, das Teil der Windows-Shell-API ist. Mit diesem Objekt können Sie über die [**iactivedesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) -Schnittstelle Elemente auf dem Desktop hinzufügen, entfernen und ändern.

## <a name="overview-of-the-active-desktop-interface"></a>Übersicht über die aktive Desktop Schnittstelle

-   [Zugreifen auf den aktiven Desktop](#accessing-the-active-desktop)
-   [Hinzufügen eines Desktop Elements](#adding-a-desktop-item)
-   [Auflisten der Desktop Elemente](#enumerating-the-desktop-items)

Der aktive Desktop ist eine in Microsoft Internet Explorer 4,0 eingeführte Funktion, mit der Sie HTML-Dokumente und-Elemente (z. b. Microsoft ActiveX-Steuerelemente und Java-Applets) direkt auf Ihren Desktop einbinden können. Die [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstelle, die Teil der Windows-Shell-API ist, wird verwendet, um die Elemente auf dem Desktop Programm gesteuert hinzuzufügen, zu entfernen und zu ändern. Aktive Desktop Elemente können auch mithilfe einer CDF-Datei (Channel Definition Format) hinzugefügt werden.

### <a name="accessing-the-active-desktop"></a>Zugreifen auf den aktiven Desktop

Um auf den aktiven Desktop zuzugreifen, muss eine Client Anwendung eine Instanz des activedesktop-Objekts (CLSID \_ activedesktop) mit der [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion erstellen und einen Zeiger auf die [**iactivedesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) -Schnittstelle des Objekts abrufen.

Im folgenden Beispiel wird gezeigt, wie ein Zeiger auf die [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstelle abgerufen wird.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>Hinzufügen eines Desktop Elements

Es gibt drei Methoden, mit denen Sie ein Desktop Element hinzufügen können: [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**iactivedesktop:: adddesktopitemwithui**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)und [**iactivedesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Jedes Desktop Element, das dem aktiven Desktop hinzugefügt wird, muss über eine andere Quell-URL verfügen.

Mit der [**iactivedesktop:: adddesktopitemwithui**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) -Methode und der [**iactivedesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) -Methode können die verschiedenen Benutzeroberflächen angezeigt werden, die angezeigt werden können, bevor dem aktiven Desktop ein Desktop Element hinzugefügt wird. Überprüfen Sie, ob Benutzer das Desktop Element dem aktiven Desktop hinzufügen möchten. Die Schnittstellen Benachrichtigen auch Benutzer über etwaige Sicherheitsrisiken, die durch die Einstellungen der URL-Sicherheitszone gewährleistet werden, und Fragen Benutzer, ob Sie ein Abonnement für dieses Desktop Element erstellen möchten. Beide Methoden bieten auch eine Möglichkeit, die Benutzeroberflächen zu unterdrücken. Die [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) -Methode erfordert einen [**iactivedesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) -Anrufe, um die Registrierung zu aktualisieren. Für **iactivedesktop:: adddesktopitemwithui** muss die Client Anwendung die [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstelle sofort freigeben und dann die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwenden, um eine Schnittstelle zu einer Instanz des **activedesktop** -Objekts abzurufen, das das neu hinzugefügte Desktop Element enthält.

Die [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) -Methode fügt das angegebene Desktop Element dem aktiven Desktop ohne Benutzeroberfläche hinzu, es sei denn, die URL-Sicherheitszonen Einstellungen verhindern dies. Wenn die URL-Sicherheitszonen Einstellungen nicht zulassen, dass das Desktop Element hinzugefügt wird, ohne den Benutzer aufzufordern, schlägt die Methode fehl. **Iactivedesktop:: adddesktopitem** erfordert auch einen [**iactivedesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) -Anrufe, um die Registrierung zu aktualisieren.

Im folgenden Beispiel wird veranschaulicht, wie Sie ein Desktop Element mit der [**iactivedesktop:: adddesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) -Methode hinzufügen.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>Auflisten der Desktop Elemente

Zum Auflisten der aktuell auf dem aktiven Desktop installierten Desktop Elemente muss die Client Anwendung die Gesamtzahl der mithilfe der [**iactivedesktop:: getdesktopitemcount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) -Methode installierten Desktop Elemente abrufen und dann eine Schleife erstellen, die die [**Komponenten**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) Struktur für jedes Desktop Element abruft, indem die [**iactivedesktop:: getdesktopitem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) -Methode mithilfe des Desktop Element Indexes aufgerufen wird.

Im folgenden Beispiel wird eine Möglichkeit zum Auflisten der Desktop Elemente veranschaulicht.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 
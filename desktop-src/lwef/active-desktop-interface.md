---
title: Verwenden des Active Desktop-Objekts
description: Dieser Artikel enthält Informationen zum ActiveDesktop-Objekt, das Teil der Windows Shell-API ist. Mit diesem Objekt können Sie über die IActiveDesktop-Schnittstelle Elemente auf dem Desktop hinzufügen, entfernen und ändern.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- ActiveDesktop-Objekt
- Active Desktop
- Enumeration, Desktopelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6daf1b5fbc73286619f07c8af76fbbce53bcaa8962cc88cf20f5af74bbdec82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610660"
---
# <a name="using-the-active-desktop-object"></a>Verwenden des Active Desktop-Objekts

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. \]

Dieser Artikel enthält Informationen zum **ActiveDesktop-Objekt,** das Teil der Windows Shell-API ist. Mit diesem Objekt können Sie über die [**IActiveDesktop-Schnittstelle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Elemente auf dem Desktop hinzufügen, entfernen und ändern.

## <a name="overview-of-the-active-desktop-interface"></a>Übersicht über die Active Desktop-Schnittstelle

-   [Zugreifen auf die Active Desktop](#accessing-the-active-desktop)
-   [Hinzufügen eines Desktopelements](#adding-a-desktop-item)
-   [Aufzählen der Desktopelemente](#enumerating-the-desktop-items)

Die Active Desktop ist ein Feature, das mit Microsoft Internet Explorer 4.0 eingeführt wurde und es Ihnen ermöglicht, HTML-Dokumente und -Elemente (z. B. Microsoft ActiveX Controls und Java-Applets) direkt in Ihren Desktop einzubinden. Die [**IActiveDesktop-Schnittstelle,**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) die Teil der Windows Shell-API ist, wird verwendet, um die Elemente auf dem Desktop programmgesteuert hinzuzufügen, zu entfernen und zu ändern. Active Desktop Elemente können auch mithilfe einer CDF-Datei (Channel Definition Format) hinzugefügt werden.

### <a name="accessing-the-active-desktop"></a>Zugreifen auf die Active Desktop

Um auf die Active Desktop zugreifen zu können, muss eine Clientanwendung eine Instanz des ActiveDesktop-Objekts (CLSID \_ ActiveDesktop) mit der [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erstellen und einen Zeiger auf die [**IActiveDesktop-Schnittstelle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) des Objekts abrufen.

Das folgende Beispiel zeigt, wie ein Zeiger auf die [**IActiveDesktop-Schnittstelle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) abgerufen wird.


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



### <a name="adding-a-desktop-item"></a>Hinzufügen eines Desktopelements

Es gibt drei Methoden, mit denen Sie ein Desktopelement hinzufügen können: [**IActiveDesktop::AddDesktopItem,**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)und [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Jedes Desktopelement, das dem Active Desktop hinzugefügt wird, muss eine andere Quell-URL aufweisen.

Die Methoden [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) und [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) bieten beide die Möglichkeit, die verschiedenen Benutzeroberflächen anzuzeigen, die angezeigt werden können, bevor dem Active Desktop ein Desktopelement hinzugefügt wird. Die Schnittstellen überprüfen, ob Benutzer das Desktopelement ihrem Active Desktop hinzufügen möchten. Die Schnittstellen benachrichtigen Benutzer auch über alle Sicherheitsrisiken, die durch die Einstellungen der URL-Sicherheitszone garantiert werden, und fragen Benutzer, ob sie ein Abonnement für dieses Desktopelement erstellen möchten. Beide Methoden bieten auch eine Möglichkeit, die Benutzeroberflächen zu unterdrücken. Die [**IActiveDesktop::AddDesktopItem-Methode**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) erfordert einen Aufruf von [**IActiveDesktop::ApplyChanges,**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) um die Registrierung zu aktualisieren. Für **IActiveDesktop::AddDesktopItemWithUI** muss die Clientanwendung sofort die [**IActiveDesktop-Schnittstelle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) freigeben und dann die [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwenden, um eine Schnittstelle zu einer Instanz des **ActiveDesktop-Objekts** abzurufen, das das neu hinzugefügte Desktopelement enthält.

Die [**IActiveDesktop::AddDesktopItem-Methode**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) fügt das angegebene Desktopelement dem Active Desktop ohne Benutzeroberfläche hinzu, es sei denn, die EINSTELLUNGEN der URL-Sicherheitszone verhindern dies. Wenn die Einstellungen der URL-Sicherheitszone nicht zulassen, dass das Desktopelement hinzugefügt wird, ohne den Benutzer dazu aufzufordern, schlägt die -Methode fehl. **IActiveDesktop::AddDesktopItem** erfordert auch einen Aufruf von [**IActiveDesktop::ApplyChanges,**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) um die Registrierung zu aktualisieren.

Im folgenden Beispiel wird veranschaulicht, wie Sie ein Desktopelement mit der [**IActiveDesktop::AddDesktopItem-Methode**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) hinzufügen.


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



### <a name="enumerating-the-desktop-items"></a>Aufzählen der Desktopelemente

Um die desktop-Elemente aufzulisten, die derzeit auf dem Active Desktop installiert sind, muss die Clientanwendung die Gesamtzahl der Desktopelemente abrufen, die mit der [**IActiveDesktop::GetDesktopItemCount-Methode**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) installiert wurden, und dann eine Schleife erstellen, die die [**COMPONENT-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) für jedes Desktopelement abruft, indem die [**IActiveDesktop::GetDesktopItem-Methode**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) mithilfe des Desktopelementindexes aufgerufen wird.

Im folgenden Beispiel wird eine Möglichkeit zum Aufzählen der Desktopelemente veranschaulicht.


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



 

 
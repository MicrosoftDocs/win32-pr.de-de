---
description: Laden einer Graph aus einem externen Prozess
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Laden einer Graph aus einem externen Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e92fdaebb9ce3cb6615153daf66a8991477bf76e16ac3298e8e8b2fb59d74b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831055"
---
# <a name="loading-a-graph-from-an-external-process"></a>Laden einer Graph aus einem externen Prozess

GraphEdit kann ein Von einem externen Prozess erstelltes Filterdiagramm laden. Mit diesem Feature können Sie genau sehen, welches Filterdiagramm Ihre Anwendung erstellt, mit nur einer minimalen Menge an zusätzlichem Code in Ihrer Anwendung.

> [!Note]  
> Dieses Feature erfordert Windows 2000, Windows XP oder höher.

 

> [!Note]  
> Ab Windows Vista müssen Sie proppage.dll registrieren, um dieses Feature zu aktivieren. Proppage.dll ist im Windows SDK enthalten.

 

Die Anwendung muss die Filterdiagramminstanz in der Running Object Table (ROT) registrieren. Rot ist eine global zugängliche Nachverfolgungstabelle, die ausgeführte Objekte nachverfolgt. Objekte werden im ROT-Moniker registriert. Um eine Verbindung mit dem Diagramm herzustellen, durchsucht GraphEdit rot nach Monikern, deren Anzeigename einem bestimmten Format entspricht:


```C++
!FilterGraph X pid Y
```



Wobei *X* die hexadezimale Adresse des Filter-Graph-Managers und *Y* die Prozess-ID ist, ebenfalls in hexadezimaler Form.

Wenn Ihre Anwendung das Filterdiagramm zum ersten Mal erstellt, rufen Sie die folgende Funktion auf:


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



Diese Funktion erstellt einen Moniker und einen neuen ROT-Eintrag für das Filterdiagramm. Der erste Parameter ist ein Zeiger auf das Filterdiagramm. Der zweite Parameter empfängt einen Wert, der den neuen ROT-Eintrag identifiziert. Bevor die Anwendung das Filterdiagramm frei gibt, rufen Sie die folgende Funktion auf, um den ROT-Eintrag zu entfernen. Der *pdwRegister-Parameter* ist der bezeichner, der von der AddToRot-Funktion zurückgegeben wird.


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



Das folgende Codebeispiel zeigt, wie diese Funktionen aufruft. In diesem Beispiel wird der Code, der ROT-Einträge hinzufügt und entfernt, bedingt kompiliert, sodass er nur in Debugbuilds enthalten ist.


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



Um das Filterdiagramm in GraphEdit anzeigen zu können, führen Sie ihre Anwendung und GraphEdit gleichzeitig aus. Klicken Sie im Menü GraphDatei **bearbeiten** auf Verbinden **remote Graph...** Wählen Sie **im Verbinden Dialogfeld Graph** die Prozess-ID (PID) Ihrer Anwendung aus, und klicken Sie auf **OK.** GraphEdit lädt das Filterdiagramm und zeigt es an. Verwenden Sie keine anderen GraphEdit-Features in diesem Diagramm. Dies kann zu unerwarteten Ergebnissen führen. Fügen Sie z. B. keine Filter hinzu oder entfernen Sie sie nicht, oder beenden und starten Sie den Graphen. Schließen Sie GraphEdit, bevor Sie Ihre Anwendung beenden.

> [!Note]  
> Ihre Anwendung kann beim Beenden auf verschiedene Asserts treffen. Sie können diese Fehler ignorieren.

 

Die folgende Abbildung zeigt das **dialogfeld Verbinden To Graph** (Zu Graph).

![Herstellen einer Verbindung mit graph](images/gedit-spy.png)

Wenn GraphEdit das Diagramm lädt, wird es im Kontext der Zielanwendung ausgeführt. Daher kann GraphEdit blockiert werden, da es auf den Thread wartet. Dies kann z. B. auftreten, wenn Sie den Code im Debugger ausführen.

Dieses Feature sollte nur in Debugbuilds Ihrer Anwendung und nicht in Einzelhandelsbuilds verwendet werden, da es anderen Anwendungen ermöglicht, das Filterdiagramm zu anzeigen oder zu steuern.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Herstellen einer Verbindung mit einem remote Graph über die Befehlszeile

GraphEdit unterstützt eine Befehlszeilenoption zum automatischen Laden eines Remotediagramms beim Start. Die Syntax ist:


```C++
GraphEdt -a moniker
```



Wobei *der Moniker* ein Moniker ist, der mit der zuvor beschriebenen AddToRot-Funktion erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Simulieren von Graph Building mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 




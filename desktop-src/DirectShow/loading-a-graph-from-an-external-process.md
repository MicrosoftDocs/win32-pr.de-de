---
description: Laden eines Diagramms aus einem externen Prozess
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Laden eines Diagramms aus einem externen Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551414"
---
# <a name="loading-a-graph-from-an-external-process"></a>Laden eines Diagramms aus einem externen Prozess

GraphEdit kann ein von einem externen Prozess erstelltes Filter Diagramm laden. Mit dieser Funktion können Sie genau sehen, welches Filter Diagramm für Ihre Anwendung erstellt wird, und zwar nur über einen minimalen zusätzlichen Code in Ihrer Anwendung.

> [!Note]  
> Für dieses Feature ist Windows 2000, Windows XP oder höher erforderlich.

 

> [!Note]  
> Ab Windows Vista müssen Sie proppage.dll registrieren, um dieses Feature zu aktivieren. Proppage.dll ist im Windows SDK enthalten.

 

Die Anwendung muss die Filter Diagramm Instanz in der laufenden Objekttabelle (rot) registrieren. Die rot ist eine Global zugängliche Nachschlage Tabelle, in der die Ausführung von Objekten nachverfolgt wird. Objekte werden im Rot von Moniker registriert. Um eine Verbindung mit dem Diagramm herzustellen, durchsucht GraphEdit die rot nach Monikern, deren Anzeige Name mit einem bestimmten Format übereinstimmt:


```C++
!FilterGraph X pid Y
```



Dabei steht *X* für die hexadezimale Adresse des Filter Graph-Managers, und *Y* für die Prozess-ID, auch als hexadezimal.

Wenn Ihre Anwendung das Filter Diagramm erstmalig erstellt, müssen Sie die folgende Funktion aufzurufen:


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



Diese Funktion erstellt einen Moniker und einen neuen rot-Eintrag für das Filter Diagramm. Der erste Parameter ist ein Zeiger auf das Filter Diagramm. Der zweite Parameter erhält einen Wert, der den neuen rot-Eintrag identifiziert. Bevor die Anwendung das Filter Diagramm freigibt, wird die folgende Funktion aufgerufen, um den rot-Eintrag zu entfernen. Der *pdwregister* -Parameter ist der Bezeichner, der von der addtorot-Funktion zurückgegeben wird.


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



Im folgenden Codebeispiel wird gezeigt, wie diese Funktionen aufgerufen werden. In diesem Beispiel wird der Code, mit dem rot-Einträge hinzugefügt und entfernt werden, bedingt kompiliert, sodass er nur in Debugbuilds enthalten ist.


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



Um das Filter Diagramm in GraphEdit anzuzeigen, führen Sie Ihre Anwendung und GraphEdit gleichzeitig aus. Klicken Sie im Menü "GraphEdit- **Datei** " auf **mit Remote Diagramm verbinden...** Wählen Sie im Dialogfeld **Verbindung mit Graph herstellen** die Prozess-ID (PID) Ihrer Anwendung aus, und klicken Sie auf **OK**. GraphEdit lädt das Filter Diagramm und zeigt es an. Verwenden Sie in diesem Diagramm keine anderen GraphEdit-Funktionen – Dies kann zu unerwarteten Ergebnissen führen. Fügen Sie z. b. keine Filter hinzu, oder entfernen Sie die Filter, und starten Sie das Diagramm nicht. Schließen Sie GraphEdit, bevor Sie die Anwendung verlassen.

> [!Note]  
> Die Anwendung kann beim Beenden verschiedene Bestätigungen erreichen. Sie können diese Fehler ignorieren.

 

Die folgende Abbildung zeigt das Dialogfeld **Verbindung mit Graph herstellen** .

![mit Diagramm verbinden](images/gedit-spy.png)

Wenn GraphEdit das Diagramm lädt, wird es im Kontext der Zielanwendung ausgeführt. Daher kann GraphEdit blockieren, weil es auf den Thread wartet. Dies kann z. b. vorkommen, wenn Sie den Code im Debugger schrittweise durchlaufen.

Diese Funktion sollte nur in Debugbuilds der Anwendung und nicht in Einzelhandels Builds verwendet werden, da es anderen Anwendungen ermöglicht, das Filter Diagramm anzuzeigen oder zu steuern.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Herstellen einer Verbindung mit einem Remote Diagramm über die Befehlszeile

GraphEdit unterstützt eine Befehlszeilenoption zum automatischen Laden eines Remote Diagramms beim Start. Die Syntax lautet:


```C++
GraphEdt -a moniker
```



Dabei ist der *Moniker* ein Moniker, der mithilfe der zuvor beschriebenen addtorot-Funktion erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Simulieren der Diagramm Erstellung mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 




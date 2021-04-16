---
description: Gelegentlich tritt eine Situation auf, in der eine Nachricht nicht erfolgreich an das beabsichtigte Ziel übermittelt werden kann. Dies ist normalerweise auf ein Problem mit dem System oder der Konfiguration zurückzuführen.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Behandeln von Fehlern in in der Warteschlange befindlichen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523872"
---
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="3f2bb-103">Behandeln von Fehlern in in der Warteschlange befindlichen Komponenten</span><span class="sxs-lookup"><span data-stu-id="3f2bb-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="3f2bb-104">Gelegentlich tritt eine Situation auf, in der eine Nachricht nicht erfolgreich an das beabsichtigte Ziel übermittelt werden kann. Dies ist normalerweise auf ein Problem mit dem System oder der Konfiguration zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="3f2bb-105">Beispielsweise kann die Nachricht an eine Warteschlange weitergeleitet werden, die nicht vorhanden ist, oder die Ziel Warteschlange befindet sich möglicherweise nicht in einem Zustand, der empfangen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="3f2bb-106">Der Nachrichten Verschiebungsvorgang ist ein Tool, das alle fehlgeschlagenen [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Nachrichten von einer Warteschlange in eine andere verschiebt, damit Sie wiederholt werden können.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="3f2bb-107">Das Hilfsprogramm für den Nachrichten Verschiebungsvorgang ist ein Automatisierungs Objekt, das mit einem VBScript aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="3f2bb-108">Komponenten Dienste-Verwaltungs Tool</span><span class="sxs-lookup"><span data-stu-id="3f2bb-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="3f2bb-109">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3f2bb-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3f2bb-110">Visual Basic</span></span>

<span data-ttu-id="3f2bb-111">Der folgende Beispielcode zeigt, wie ein messagemover-Objekt erstellt, die erforderlichen Eigenschaften festgelegt und die Übertragung initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="3f2bb-112">Um es aus Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="3f2bb-113">Um das messagemover-Objekt verwenden zu können, müssen Message Queuing auf dem Computer installiert sein, und für die in appname angegebene Anwendung muss die Warteschlange aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="3f2bb-114">Weitere Informationen zum Installieren von Message Queuing finden Sie unter Hilfe und Support im **Startmenü** .</span><span class="sxs-lookup"><span data-stu-id="3f2bb-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



<span data-ttu-id="3f2bb-115">Der folgende Visual Basic Code zeigt, wie die mymessagemover-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="3f2bb-116">Der Quellpfad der Nachricht ist die letzte ruhende Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="3f2bb-117">Dabei handelt es sich um die Warteschlange für unzustellbare Nachrichten, bei der es sich um eine private Message Queuing Warteschlange handelt und \_</span><span class="sxs-lookup"><span data-stu-id="3f2bb-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="3f2bb-118">Nachrichten werden hier verschoben, wenn die Transaktion bei einem Versuch in der fünften Wiederholungs Warteschlange wiederholt abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="3f2bb-119">Mit dem Message Verschiebungs Tool können Sie die Nachricht zurück in die erste Warteschlange verschieben, die als appname bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="3f2bb-120">Weitere Informationen zu Wiederholungs Warteschlangen finden Sie unter [Server seitige Fehler](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3f2bb-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="3f2bb-121">Wenn Queue-Attribute zulässig sind, verschiebt der Nachrichten Verschiebungs Vorgang die Nachrichten transitiv, sodass Nachrichten im Fall eines Fehlers während der Verschiebung nicht verloren gehen oder dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="3f2bb-122">Das Tool behält alle Nachrichten Eigenschaften bei, die beibehalten werden können, wenn Nachrichten von einer Warteschlange in eine andere verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="3f2bb-123">Wenn die Nachrichten von com+-in der Warteschlange befindlichen Komponenten aufgerufen werden, behält das Nachrichten verschiebungsprogramm die Sicherheits-ID des ursprünglichen Aufrufers bei, während Nachrichten zwischen Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="3f2bb-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="3f2bb-124">Wenn sowohl die Ziel-als auch die Quell Warteschlange transaktional sind, erfolgt der gesamte Vorgang transitiv.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="3f2bb-125">Wenn die Quell-oder Ziel Warteschlange nicht transaktional sind, wird der Vorgang nicht unter einer Transaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="3f2bb-126">Ein unerwarteter Fehler (z. b. ein Absturz) und ein Neustart eines nicht transaktionalen Verschiebens können das Verschieben der Nachricht zum Zeitpunkt des Fehlers duplizieren.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="3f2bb-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="3f2bb-127">C/C++</span></span>

<span data-ttu-id="3f2bb-128">Der folgende Beispielcode zeigt, wie ein messagemover-Objekt erstellt, die erforderlichen Eigenschaften festgelegt und die Übertragung initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="3f2bb-129">Die ErrorDescription-Methode wird unter [Interpretieren von Fehler Codes](interpreting-error-codes.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="3f2bb-130">Um das messagemover-Objekt verwenden zu können, müssen Message Queuing auf dem Computer installiert sein, und für die in appname angegebene Anwendung muss die Warteschlange aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="3f2bb-131">Weitere Informationen zum Installieren von Message Queuing finden Sie unter Hilfe und Support im **Startmenü** .</span><span class="sxs-lookup"><span data-stu-id="3f2bb-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



<span data-ttu-id="3f2bb-132">Der folgende C++-Code zeigt, wie die mymessagemover-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



<span data-ttu-id="3f2bb-133">Der Quellpfad der Nachricht ist die letzte ruhende Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="3f2bb-134">Dabei handelt es sich um die Warteschlange für unzustellbare Nachrichten, bei der es sich um eine private Message Queuing Warteschlange handelt und \_</span><span class="sxs-lookup"><span data-stu-id="3f2bb-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="3f2bb-135">Nachrichten werden hier verschoben, wenn die Transaktion bei einem Versuch in der fünften Wiederholungs Warteschlange wiederholt abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="3f2bb-136">Mit dem Message Verschiebungs Tool können Sie die Nachricht zurück in die erste Warteschlange verschieben, die als appname bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="3f2bb-137">Weitere Informationen zu Wiederholungs Warteschlangen finden Sie unter [Server seitige Fehler](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3f2bb-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="3f2bb-138">Wenn Queue-Attribute zulässig sind, verschiebt der Nachrichten Verschiebungs Vorgang die Nachrichten transitiv, sodass Nachrichten im Fall eines Fehlers während der Verschiebung nicht verloren gehen oder dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="3f2bb-139">Das Tool behält alle Nachrichten Eigenschaften bei, die beibehalten werden können, wenn Nachrichten von einer Warteschlange in eine andere verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="3f2bb-140">Wenn die Nachrichten von com+-in der Warteschlange befindlichen Komponenten aufgerufen werden, behält das Nachrichten verschiebungsprogramm die Sicherheits-ID des ursprünglichen Aufrufers bei, während Nachrichten zwischen Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="3f2bb-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="3f2bb-141">Wenn sowohl die Ziel-als auch die Quell Warteschlange transaktional sind, erfolgt der gesamte Vorgang transitiv.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="3f2bb-142">Wenn die Quell-oder Ziel Warteschlange nicht transaktional sind, wird der Vorgang nicht unter einer Transaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="3f2bb-143">Ein unerwarteter Fehler (z. b. ein Absturz) und ein Neustart eines nicht transaktionalen Verschiebens können das Verschieben der Nachricht zum Zeitpunkt des Fehlers duplizieren.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2bb-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f2bb-144">Remarks</span></span>

<span data-ttu-id="3f2bb-145">Com+ verarbeitet serverseitige (Player-) Abbrüche, indem die Nachricht, bei der ein Fehler auftritt, in eine andere "abschließende ruhende" Warteschlange verschoben wird, um Sie zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="3f2bb-146">Der Listener und der Player können eine Nachricht, die abgebrochen wird, nicht fortlaufend Schleifen.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="3f2bb-147">In vielen Fällen kann die abgebrochene Transaktion korrigiert werden, indem eine Aktion auf dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f2bb-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f2bb-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f2bb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f2bb-149">Komponenten Fehler in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="3f2bb-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 




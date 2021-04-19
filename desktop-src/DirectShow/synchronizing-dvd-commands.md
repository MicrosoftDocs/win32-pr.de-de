---
description: Synchronisieren von DVD-Befehlen
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Synchronisieren von DVD-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362710"
---
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="f539a-103">Synchronisieren von DVD-Befehlen</span><span class="sxs-lookup"><span data-stu-id="f539a-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="f539a-104">DVD-Befehle sind nicht immer sofort fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="f539a-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="f539a-105">Aus diesem Grund sind einige der Methoden in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) asynchron.</span><span class="sxs-lookup"><span data-stu-id="f539a-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="f539a-106">Dazu zählen Wiedergabe Methoden wie **playtitle** und Menü Navigationsmethoden, z. b. **showmenu** und **returnfromsubmenu**.</span><span class="sxs-lookup"><span data-stu-id="f539a-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="f539a-107">Eine asynchrone Methode wird sofort zurückgegeben, ohne auf den Abschluss des Befehls zu warten.</span><span class="sxs-lookup"><span data-stu-id="f539a-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="f539a-108">Nachdem die-Methode zurückgegeben wurde, können andere Ereignisse den Abschluss des Befehls verhindern, auch wenn die Methode erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f539a-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="f539a-109">DirectShow bietet verschiedene Optionen zum Synchronisieren von Befehlen, die von der Synchronisierung bis zur vollständigen Synchronisierung mithilfe von Filter Diagramm Ereignissen reichen.</span><span class="sxs-lookup"><span data-stu-id="f539a-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="f539a-110">Alle asynchronen Methoden verfügen über einen *dwFlags* -Parameter und einen *ppcmd* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="f539a-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="f539a-111">Der *dwFlags* -Parameter gibt das Synchronisierungs Verhalten an, und der *ppcmd* -Parameter gibt einen Zeiger auf ein optionales Synchronisierungs Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f539a-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="f539a-112">Je nachdem, welche Werte Sie für diese Parameter angeben, gibt es unterschiedliche Verhaltensweisen.</span><span class="sxs-lookup"><span data-stu-id="f539a-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="f539a-113">**Keine Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="f539a-113">**No Synchronization**</span></span>

<span data-ttu-id="f539a-114">Bei einer einfachen DVD-Wiedergabe Anwendung ist es möglicherweise einfach, Synchronisierungs Probleme zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="f539a-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="f539a-115">Gelegentlich kann es vorkommen, dass ein Befehl fehlschlägt oder die Benutzeroberfläche bei der Aktualisierung geringfügig verzögert wird, diese Fehler jedoch in der Reihenfolge der Sekundenbruchteile liegen.</span><span class="sxs-lookup"><span data-stu-id="f539a-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="f539a-116">Um einen Befehl ohne Synchronisierung auszugeben, legen Sie das DVD- \_ cmd \_ -Flag " \_ None" im *dwFlags* -Parameter fest, und legen Sie den *ppcmd* -Parameter auf **null** fest:</span><span class="sxs-lookup"><span data-stu-id="f539a-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="f539a-117">**Blockierung**</span><span class="sxs-lookup"><span data-stu-id="f539a-117">**Blocking**</span></span>

<span data-ttu-id="f539a-118">Wenn Sie das \_ schlüsselblockflag für die EC-DVD \_ \_ \_ im *dwFlags* -Parameter festlegen, wird die-Methode blockiert, bis der Befehl abgeschlossen ist:</span><span class="sxs-lookup"><span data-stu-id="f539a-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="f539a-119">Dieses Flag wandelt eine asynchrone Methode in eine synchrone Methode um.</span><span class="sxs-lookup"><span data-stu-id="f539a-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="f539a-120">Der Nachteil ist, dass die Benutzeroberfläche blockiert wird, wenn Sie die-Methode aus dem Anwendungs Thread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f539a-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="f539a-121">**Synchronisierungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="f539a-121">**Synchronization Object**</span></span>

<span data-ttu-id="f539a-122">Alle asynchronen Methoden können ein Synchronisierungs Objekt zurückgeben, das Sie verwenden können, um auf das Starten oder Beenden des Befehls zu warten.</span><span class="sxs-lookup"><span data-stu-id="f539a-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="f539a-123">Um dieses Objekt zu erhalten, übergeben Sie die Adresse eines [**idvdcmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) -Zeigers im *ppcmd* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="f539a-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="f539a-124">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie ein neues **idvdcmd** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f539a-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="f539a-125">Die [**idvdcmd:: waitforstart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) -Methode blockiert, bis der Befehl beginnt, und die [**idvdcmd:: waitforend**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) -Methode blockiert, bis der Befehl beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f539a-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="f539a-126">Der Rückgabewert gibt den Status des Befehls an.</span><span class="sxs-lookup"><span data-stu-id="f539a-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="f539a-127">Der folgende Code ist funktional äquivalent zum Festlegen des \_ \_ \_ zuvor gezeigten Flag für das "EC-DVD-cmd-Flag" \_ .</span><span class="sxs-lookup"><span data-stu-id="f539a-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



<span data-ttu-id="f539a-128">In diesem Fall wird die **playtitle** -Methode nicht blockiert, aber die Anwendung wird durch den Aufruf von **waitforend** blockiert.</span><span class="sxs-lookup"><span data-stu-id="f539a-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="f539a-129">**Befehls Status Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="f539a-129">**Command Status Events**</span></span>

<span data-ttu-id="f539a-130">Wenn Sie \_ \_ \_ im *dwFlags* -Parameter das Flag sendevents für das DVD-cmd-Flag festlegen, sendet der DVD-Navigator ein [**EC-DVD- \_ \_ cmd- \_ Start**](ec-dvd-cmd-start.md) Ereignis, wenn der Befehl beginnt, und ein [**EC-DVD- \_ \_ cmd \_**](ec-dvd-cmd-end.md) -Ereignis, wenn der Befehl endet.</span><span class="sxs-lookup"><span data-stu-id="f539a-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="f539a-131">Der *lParam2* -Parameter des Ereignisses ist der HRESULT-Rückgabewert für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="f539a-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="f539a-132">Der *lParam1* -Parameter des Ereignisses bietet eine Möglichkeit, das Synchronisierungs Objekt für den Befehl zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f539a-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="f539a-133">Wenn Sie *lParam1* an die [**IDvdInfo2:: getcmdfromevent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) -Methode übergeben, gibt die Methode einen Zeiger auf die **idvdcmd** -Schnittstelle des Synchronisierungs Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="f539a-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="f539a-134">Sie können diese Schnittstelle verwenden, um auf den Abschluss des Befehls zu warten, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f539a-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="f539a-135">Wenn Sie jedoch **null** für den *ppcmd* -Parameter in der ursprünglichen **IDvdControl2** -Methode übergeben haben, erstellt der DVD-Navigator kein Synchronisierungs Objekt, und **getcmdfromevent** gibt E \_ Fail zurück.</span><span class="sxs-lookup"><span data-stu-id="f539a-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="f539a-136">Der folgende Code zeigt, wie Sie Befehlsstatus Ereignisse ohne Synchronisierungs Objekt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f539a-136">The following code shows how to use command status events with no synchronization object.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



<span data-ttu-id="f539a-137">Beachten Sie, dass Sie ohne Synchronisierungs Objekt nicht erkennen können, welcher Befehl dem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f539a-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="f539a-138">Der folgende Code zeigt, wie Ereignisse mit dem Synchronisierungs Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f539a-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="f539a-139">Die Idee besteht darin, die Synchronisierungs Objekte in einer Liste zu speichern und dann Objekt Zeiger zu vergleichen, wenn Sie das [**\_ \_ cmd- \_ Start**](ec-dvd-cmd-start.md) Ereignis oder das [**EC-DVD- \_ \_ cmd- \_ Endereignis**](ec-dvd-cmd-end.md) erhalten.</span><span class="sxs-lookup"><span data-stu-id="f539a-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



<span data-ttu-id="f539a-140">**Leeren der Puffer des DVD-Navigators**</span><span class="sxs-lookup"><span data-stu-id="f539a-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="f539a-141">Während der Wiedergabe puffert der DVD-Navigator Videodaten.</span><span class="sxs-lookup"><span data-stu-id="f539a-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="f539a-142">Die Menge der gepufferten Daten variiert.</span><span class="sxs-lookup"><span data-stu-id="f539a-142">The amount of buffered data varies.</span></span> <span data-ttu-id="f539a-143">Wenn der DVD-Navigator zu einem neuen Video wechselt, gehen die Daten, die sich bereits in der Pipeline befinden, nicht verloren, sodass der Übergang nahtlos verläuft.</span><span class="sxs-lookup"><span data-stu-id="f539a-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="f539a-144">Wenn der DVD-Navigator einen Befehl ausgibt, werden die in der Pipeline bereits vorhandenen Datenstandard mäßig nicht geleert.</span><span class="sxs-lookup"><span data-stu-id="f539a-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="f539a-145">Dies führt möglicherweise zu einer gewissen Latenz, bevor Sie die Auswirkungen des Befehls erkennen können, je nachdem, wie viele Daten gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="f539a-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="f539a-146">Um die Reaktionsfähigkeit zu erhöhen, können Sie erzwingen, dass der DVD-Navigator geleert wird, indem Sie das Flag "DVD \_ cmd \_ Flag Flush" festlegen \_ .</span><span class="sxs-lookup"><span data-stu-id="f539a-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="f539a-147">Dieses Flag kann mit einem der zuvor beschriebenen Flags kombiniert werden, wobei ein bitweises OR verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f539a-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="f539a-148">Ein Nebeneffekt des Leerung besteht darin, dass möglicherweise ein Video verloren geht. verwenden Sie daher dieses Flag nicht, wenn Sie sicherstellen müssen, dass keine Lücken im Video vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f539a-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f539a-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f539a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f539a-150">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f539a-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




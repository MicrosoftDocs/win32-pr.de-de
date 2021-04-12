---
title: Registrieren eines com-Rückrufs
description: Anstatt Änderungen am Status eines Auftrags abzufragen, können Sie sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich der Status des Auftrags ändert.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- Übertragen von Auftrags Bits, Ereignis Benachrichtigung
- Registrieren für Ereignis Benachrichtigungs Bits
- Ereignis Benachrichtigungs Bits
- Ereignis Benachrichtigungs Bits, Rückrufe
- Bits von Benachrichtigungs Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315693"
---
# <a name="registering-a-com-callback"></a><span data-ttu-id="b01e9-108">Registrieren eines com-Rückrufs</span><span class="sxs-lookup"><span data-stu-id="b01e9-108">Registering a COM Callback</span></span>

<span data-ttu-id="b01e9-109">Anstatt Änderungen am [Status eines Auftrags](polling-for-the-status-of-the-job.md) abzufragen, können Sie sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich der Status des Auftrags ändert.</span><span class="sxs-lookup"><span data-stu-id="b01e9-109">Instead of [polling](polling-for-the-status-of-the-job.md) for changes in the status of a job, you can register to receive notification when the job's status changes.</span></span> <span data-ttu-id="b01e9-110">Um Benachrichtigungen zu erhalten, müssen Sie die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="b01e9-110">To receive notification, you must implement the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface.</span></span> <span data-ttu-id="b01e9-111">Die-Schnittstelle enthält die folgenden Methoden, die von Bits aufgerufen werden, abhängig von Ihrer Registrierung:</span><span class="sxs-lookup"><span data-stu-id="b01e9-111">The interface contains the following methods that BITS calls, depending on your registration:</span></span>

-   [<span data-ttu-id="b01e9-112">**Jobübertragene**</span><span class="sxs-lookup"><span data-stu-id="b01e9-112">**JobTransferred**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [<span data-ttu-id="b01e9-113">**Joberror**</span><span class="sxs-lookup"><span data-stu-id="b01e9-113">**JobError**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [<span data-ttu-id="b01e9-114">**Jobmodifizierung**</span><span class="sxs-lookup"><span data-stu-id="b01e9-114">**JobModification**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [<span data-ttu-id="b01e9-115">**Filetransfer**</span><span class="sxs-lookup"><span data-stu-id="b01e9-115">**FileTransferred**</span></span>](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

<span data-ttu-id="b01e9-116">Ein Beispiel, in dem die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle implementiert wird, finden Sie im Beispielcode im Thema [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b01e9-116">For an example that implements the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface, see the example code in the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface topic.</span></span>

<span data-ttu-id="b01e9-117">Die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle stellt Benachrichtigungen bereit, wenn eine Datei übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="b01e9-117">The [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface provides notification when a file is transferred.</span></span> <span data-ttu-id="b01e9-118">Normalerweise verwenden Sie diese Methode, um die Datei zu validieren, damit die Datei für Peers verfügbar ist, um sie herunterzuladen. Andernfalls ist die Datei für Peers nicht verfügbar, bis Sie die Methode [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="b01e9-118">Typically, you use this method to validate the file, so that the file is available for peers to download; otherwise, the file is not available to peers until you call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="b01e9-119">Um die Datei zu überprüfen, müssen Sie die [**IBackgroundCopyFile3:: setvalidationstate**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b01e9-119">To validate the file, call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method.</span></span>

<span data-ttu-id="b01e9-120">Es gibt zwei Methoden zum Registrieren eines com-Rückrufs: das Registrieren eines Rückruf Objekts oder das Registrieren einer Rückruf Klassen-ID.</span><span class="sxs-lookup"><span data-stu-id="b01e9-120">There are two methods for registering a COM callback: registering a callback object, or registering a callback class ID.</span></span> <span data-ttu-id="b01e9-121">Die Verwendung eines Rückruf Objekts ist einfacher und geringerer Aufwand. die Verwendung einer Rückruf-CLSID ist zuverlässiger, aber komplizierter.</span><span class="sxs-lookup"><span data-stu-id="b01e9-121">Using a callback object is simpler and lower overhead; using a callback CLSID is more reliable, but more complicated.</span></span> <span data-ttu-id="b01e9-122">Sie können entweder, beides oder keines von beiden – Bits verwendet ein Rückruf Objekt, wenn ein solches vorhanden ist und weiterhin aufgerufen werden kann. wenn dies nicht der Fall ist, wird ein neues Objekt auf der Grundlage einer bereitgestellten Klassen-ID instanziiert.</span><span class="sxs-lookup"><span data-stu-id="b01e9-122">You can register either, both, or neither – BITS will use a callback object if one exists and can still be called, and will fall back to instantiating a new object based on a provided class ID if that fails.</span></span>

### <a name="registering-a-callback-object"></a><span data-ttu-id="b01e9-123">Registrieren eines Rückruf Objekts</span><span class="sxs-lookup"><span data-stu-id="b01e9-123">Registering a Callback Object</span></span>

<span data-ttu-id="b01e9-124">Um die Implementierung mit Bits zu registrieren, müssen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b01e9-124">To register your implementation with BITS, call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method.</span></span> <span data-ttu-id="b01e9-125">Um anzugeben, welche Methoden Bits aufruft, rufen Sie die [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b01e9-125">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)method.</span></span>

<span data-ttu-id="b01e9-126">Die Benachrichtigungs Schnittstelle wird ungültig, wenn die Anwendung beendet wird. Bits behält die Benachrichtigungs Schnittstelle nicht bei.</span><span class="sxs-lookup"><span data-stu-id="b01e9-126">The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface.</span></span> <span data-ttu-id="b01e9-127">Folglich sollte der Initialisierungs Prozess ihrer Anwendung vorhandene Aufträge registrieren, für die Sie eine Benachrichtigung erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="b01e9-127">As a result, your application's initialization process should register existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="b01e9-128">Wenn Sie Zustands-und Statusinformationen erfassen müssen, die seit der letzten Ausführung der Anwendung aufgetreten sind, rufen Sie während der Anwendungs Initialisierung Informationen zum Status und zum Fortschritt ab.</span><span class="sxs-lookup"><span data-stu-id="b01e9-128">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="b01e9-129">Bevor die Anwendung beendet wird, sollte Sie den Rückruf Schnittstellen Zeiger (**setnotifyinterface (null)**) löschen.</span><span class="sxs-lookup"><span data-stu-id="b01e9-129">Before exiting, your application should clear the callback interface pointer (**SetNotifyInterface(NULL)**).</span></span> <span data-ttu-id="b01e9-130">Es ist effizienter, den Rückruf Zeiger zu löschen, als Bits feststellen zu können, dass er nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b01e9-130">It is more efficient to clear the callback pointer than to let BITS discover that it is no longer valid.</span></span>

<span data-ttu-id="b01e9-131">Beachten Sie Folgendes: Wenn mehr als eine Anwendung die [**setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode aufruft, um die Benachrichtigungs Schnittstelle für den Auftrag festzulegen, ist die letzte Anwendung, die die **setnotifyinterface** -Methode aufruft, die, die Benachrichtigungen empfängt – die anderen Anwendungen erhalten keine Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="b01e9-131">Note that if more than one application calls the [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to set the notification interface for the job, the last application to call the **SetNotifyInterface** method is the one that will receive notifications—the other applications will not receive notifications.</span></span>

<span data-ttu-id="b01e9-132">Im folgenden Beispiel wird gezeigt, wie Sie sich für Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="b01e9-132">The following example shows how to register for notifications.</span></span> <span data-ttu-id="b01e9-133">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b01e9-133">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span> <span data-ttu-id="b01e9-134">Ausführliche Informationen zur cnotifyinterface-Beispiel Klasse, die im folgenden Beispiel verwendet wird, finden Sie unter [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b01e9-134">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a><span data-ttu-id="b01e9-135">Registrieren einer Rückruf-CLSID</span><span class="sxs-lookup"><span data-stu-id="b01e9-135">Registering a Callback CLSID</span></span>

<span data-ttu-id="b01e9-136">Um eine Rückruf-CLSID mit Bits zu registrieren, rufen Sie die [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) -Methode mit der **\_ \_ \_ Benachrichtigung \_ CLSID** PropertyId für die Bits-Auftrags Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="b01e9-136">To register a callback CLSID with BITS, call the [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) method with the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** PropertyId.</span></span> <span data-ttu-id="b01e9-137">Um anzugeben, welche Methoden Bits aufruft, rufen Sie die [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b01e9-137">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method.</span></span>

<span data-ttu-id="b01e9-138">Sie müssen sicherstellen, dass die Benachrichtigungs-CLSID bei einem Out-of-Process-COM-Server registriert wird, bevor die CLSID bei einem BITS-Auftrag registriert wird.</span><span class="sxs-lookup"><span data-stu-id="b01e9-138">You must ensure that the notification CLSID is registered to an out-of-process COM server prior to registering the CLSID with a BITS job.</span></span> <span data-ttu-id="b01e9-139">Das Implementieren eines [com-Servers](/windows/desktop/com/com-server-responsibilities) ist wesentlich komplizierter als das definieren und übergeben eines Rückruf Objekts, bietet jedoch einige wichtige Vorteile.</span><span class="sxs-lookup"><span data-stu-id="b01e9-139">Implementing a [COM server](/windows/desktop/com/com-server-responsibilities) is significantly more complicated than defining and passing a callback object, but offers several important advantages.</span></span> <span data-ttu-id="b01e9-140">Mit einem com-Server können Bits die Zuordnung zwischen einem BITS-Auftrag und dem Code Ihrer Anwendung über Systemneustarts hinweg und für große oder langlebige Aufträge hinweg aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="b01e9-140">A COM server allows BITS to maintain the association between a BITS job and your application’s code across system reboots, and for large or long-lived jobs.</span></span> <span data-ttu-id="b01e9-141">Ein com-Server ermöglicht außerdem, dass Ihre Anwendung vollständig heruntergefahren wird, während Bits die Ausführung von Übertragungen im Hintergrund fortsetzt, wodurch die Akku-, CPU-und Speicherauslastung des Systems verbessert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b01e9-141">A COM server also allows your application to shut down completely while BITS continues executing transfers in the background, which can improve battery, CPU, and memory usage of the system.</span></span>

<span data-ttu-id="b01e9-142">Um eine Benachrichtigung bereitzustellen, die Sie für den Empfang registriert haben, versucht Bits zuerst, die entsprechende Methode eines beliebigen vorhandenen Rückruf Objekts aufzurufen, das Sie möglicherweise angefügt haben.</span><span class="sxs-lookup"><span data-stu-id="b01e9-142">To provide a notification you have registered to receive, BITS first attempts to call the corresponding method of any existing callback object you may have attached.</span></span> <span data-ttu-id="b01e9-143">Wenn kein vorhandenes Objekt vorhanden ist, wenn das vorhandene Objekt getrennt wurde (in der Regel aufgrund der Beendigung der Anwendung), ruft Bits mithilfe der Benachrichtigungs-CLSID ein neues Rückruf Objekt ab und verwendet dieses Objekt für alle weiteren Rückrufe, bis es getrennt wird, oder es wird durch einen neuen [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)-Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b01e9-143">If there is no existing object, or if that existing object has become disconnected (typically as a result of your application terminating), BITS will call CoCreateInstance using the notification CLSID to instantiate a new callback object, and will use that object for any further callbacks until it becomes disconnected or it is replaced by a new call to [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span></span>

<span data-ttu-id="b01e9-144">Im Gegensatz zu Rückruf Objekten werden Rückruf-CLSID neben den entsprechenden Bits-Aufträgen persistent gespeichert, wenn der BITS-Dienst oder das System heruntergefahren und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b01e9-144">Unlike callback objects, callback CLSID are persisted alongside their corresponding BITS job(s) if the BITS service or the system are shut down and restarted.</span></span> <span data-ttu-id="b01e9-145">Die Anwendung löscht ggf. alle zuvor festgelegten Benachrichtigungs-CLSID, bevor Sie (oder zu einem anderen Zeitpunkt) beendet wird, indem Sie eine neue Benachrichtigungs-CLSID mit der GUID \_ null übergibt. Ihre Anwendung kann jedoch vorziehen, dass die Benachrichtigungs-CLSID registriert ist, wenn Ihre Anwendung registriert ist</span><span class="sxs-lookup"><span data-stu-id="b01e9-145">Your application may clear any previously-set notification CLSID before exiting (or at any other time) by passing a new notification CLSID of GUID\_NULL, but your application may prefer to leave the notification CLSID registered if your application has registered to have COM start it in response to CoCreateInstance requests for your CLSID.</span></span> <span data-ttu-id="b01e9-146">Beachten Sie Folgendes: Wenn mehr als eine Anwendung den-Wert aufruft, der die Eigenschaft **\_ \_ \_ Benachrichtigungs- \_ CLSID für Bits-Auftrags Eigenschaften** aufruft, wird die letzte CLSID festgelegt, die Bits zum Instanziieren von Rückruf Objekten verwendet – die anderen CLSIDs werden nicht instanziiert.</span><span class="sxs-lookup"><span data-stu-id="b01e9-146">Note that if more than one application sets the calls the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** property, the last CLSID to be set is the one that BITS will use to instantiate callback objects – the other CLSIDs will not be instantiated.</span></span> <span data-ttu-id="b01e9-147">Ebenso gilt: Wenn eine Anwendung eine CLSID registriert und ein anderes ein Rückruf Objekt registriert, gelten die üblichen Regeln für das Rückruf Objekt, die Vorrang haben, und die CLSID wird nur dann verwendet, wenn das Rückruf Objekt gelöscht wird oder getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="b01e9-147">Similarly, if one application registers a CLSID and another registers a callback object, the usual rules for the callback object taking precedence apply, and the CLSID will not be used unless the callback object is cleared or becomes disconnected.</span></span>

<span data-ttu-id="b01e9-148">Im folgenden Beispiel wird gezeigt, wie Sie sich für CLSID-Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="b01e9-148">The following example shows how to register for CLSID notifications.</span></span> <span data-ttu-id="b01e9-149">Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) -Schnittstellen Zeiger gültig ist und dass Ihre Anwendung bereits als Prozess interner com-Server registriert ist, der die cnotifyinterface-Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="b01e9-149">The example assumes the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface pointer is valid, and that your application has already registered as an out-of-process COM Server which implements the CNotifyInterface class.</span></span> <span data-ttu-id="b01e9-150">Ausführliche Informationen zur cnotifyinterface-Beispiel Klasse, die im folgenden Beispiel verwendet wird, finden Sie unter [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b01e9-150">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 
---
title: Abschließen und Abbrechen eines Auftrags
description: Um einen Übertragungs Auftrag abzuschließen, wenden Sie die Methode "ibackgroundcopyjob Complete" an.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- Übertragen von Auftrags Bits, Abbrechen
- Abbrechen von Auftrags Bits
- Übertragen von Auftrags Bits, abschließen
- Abschließen von Auftrags Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470980"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="fec3f-107">Abschließen und Abbrechen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="fec3f-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="fec3f-108">Um einen Übertragungs Auftrag abzuschließen, können Sie die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="fec3f-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="fec3f-109">Für Download Aufträge können Sie die **Complete** -Methode aufzurufen, bevor alle Dateien im Auftrag übertragen wurden (vor dem Status des Auftrags lautet der Status der BG- \_ Auftrags \_ \_ Übertragung).</span><span class="sxs-lookup"><span data-stu-id="fec3f-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="fec3f-110">Nur die Dateien, die von Bits vor dem Aufruf der **Complete** -Methode erfolgreich an den Client übertragen wurden, sind für den Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fec3f-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="fec3f-111">Bei Uploadaufträgen wird die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode nur aufgerufen, wenn der Status des Auftrags "BG \_ Job \_ State \_ transferi" lautet.</span><span class="sxs-lookup"><span data-stu-id="fec3f-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="fec3f-112">Um zu ermitteln, wann der Status des Auftrags "BG \_ Job \_ State \_ transferi" lautet, rufen Sie die Zustands Eigenschaft des Auftrags ab, oder registrieren Sie sich, um [die](polling-for-the-status-of-the-job.md) \_ \_ \_ [Ereignis Benachrichtigung](registering-a-com-callback.md)"BG notify notify Job</span><span class="sxs-lookup"><span data-stu-id="fec3f-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="fec3f-113">Um einen Übertragungs Auftrag abzubrechen, rufen Sie die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="fec3f-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="fec3f-114">Die **Cancel** -Methode entfernt den Auftrag aus der Übertragungs Warteschlange und entfernt die temporären Dateien vom Client.</span><span class="sxs-lookup"><span data-stu-id="fec3f-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="fec3f-115">In der Regel wird diese Methode aufgerufen, wenn Sie einen Fehler, der dem Auftrag zugeordnet ist, nicht beheben können.</span><span class="sxs-lookup"><span data-stu-id="fec3f-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="fec3f-116">Die [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode bricht einen Upload ab, wenn der Upload nicht beendet ist.</span><span class="sxs-lookup"><span data-stu-id="fec3f-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="fec3f-117">Wenn der Upload fertiggestellt ist und der Auftrag vom Typ "BG \_ Job \_ Type \_ Upload Reply" ist, wird die Antwort von \_ der Methode abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fec3f-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="fec3f-118">Wenn Sie die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode oder die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode nicht innerhalb von 90 Tagen aufrufen (Standardwert für [jobinactivitytimeout](group-policies.md) Gruppenrichtlinie), bricht der Dienst den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="fec3f-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="fec3f-119">Wenn der Dienst den Auftrag abbricht, sind die heruntergeladenen Dateien und die Antwortdatei für den Client nicht verfügbar. die Auftrags Abbruch wirkt sich nicht auf Dateien aus, die erfolgreich hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="fec3f-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="fec3f-120">Sie sollten immer die **Complete** -oder **Cancel** -Methode aufrufen und sich nicht auf die jobinactivitytimeout-Richtlinie verlassen, um die Aufträge zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="fec3f-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="fec3f-121">Die in der Warteschlange verbleibenden Aufträge können verhindern, dass Benutzer andere Aufträge erstellen, wenn das Richtlinien Limit von maxjobsperuser oder maxjobspermachine erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="fec3f-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 





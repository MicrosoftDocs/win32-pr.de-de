---
title: Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen
description: Windows-Remoteverwaltung PowerShell-Cmdlets können Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge verwalten.
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523779"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="b841d-103">Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="b841d-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="b841d-104">Windows-Remoteverwaltung PowerShell-Cmdlets können Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge verwalten.</span><span class="sxs-lookup"><span data-stu-id="b841d-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="b841d-105">Weitere Informationen zur Bits-Remote Verwaltung finden Sie unter [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) -und Bits- [Anbieter Klassen]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b841d-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="b841d-106">Die folgenden Beispiele erfordern den [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider).</span><span class="sxs-lookup"><span data-stu-id="b841d-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="b841d-107">Der Bits-Anbieter ist verfügbar, nachdem der BITS Compact-Server installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b841d-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="b841d-108">Informationen zum Installieren des Compact-Servers finden Sie in der Dokumentation zu [BITS Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="b841d-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="b841d-109">Erstellen Sie einen Bits-Übertragungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="b841d-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="b841d-110">Das [Get-Credential-](/previous-versions//dd315327(v=technet.10)) Cmdlet fordert die Anmelde Informationen des Benutzers auf, um eine Verbindung mit dem Remote Computer herzustellen, und weist die Anmelde Informationen dem $cred-Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="b841d-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="b841d-111">Das " [Aufruf-wsmanaction"-](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) Cmdlet erstellt den Bits-Übertragungs Auftrag auf CLIENT1, indem eine Instanz der Klasse " [bitsclientjob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) " erstellt und die in dem *valueset* -Parameter definierten Informationen in der Hash Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b841d-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="b841d-112">Der *valueset* -Parameter gibt die Informationen an, die erforderlich sind, um die Parameter der Methode " [kreatejob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) " aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="b841d-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="b841d-113">Im vorherigen Beispiel hat der Benutzer den *Typparameter* auf 0 (Download) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b841d-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="b841d-114">Der Benutzer gibt auch den Namen der Remote Dateien und lokalen Dateien für den Download Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b841d-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="b841d-115">Weitere Informationen zum Erstellen von Bits-Übertragungs Aufträgen und ausführliche Informationen zu Parametern finden Sie unter Methode " [kreatejob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) ".</span><span class="sxs-lookup"><span data-stu-id="b841d-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="b841d-116">Das " [Aufruf-wsmanaction"-](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet weist das Ergebnis der $Result Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="b841d-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="b841d-117">Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b841d-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="b841d-118">Legen Sie die Priorität des Bits-Übertragungs Auftrags fest.</span><span class="sxs-lookup"><span data-stu-id="b841d-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="b841d-119">Das [Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) -Cmdlet ändert die neue Bits-Übertragungs Auftrags Priorität in 0 (**BG \_ Job \_ priority \_ Vordergrund**).</span><span class="sxs-lookup"><span data-stu-id="b841d-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="b841d-120">Weitere Informationen zu den Prioritätsstufen finden Sie unter der [**BG- \_ Auftrags \_ Prioritäts**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b841d-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="b841d-121">Setzen Sie den Bits-Übertragungs Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="b841d-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="b841d-122">Das " [Aufruf-wsmanaction"-](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet ruft die [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) -Methode auf, mit der der Auftragsstatus auf 2 festgelegt wird (Fortsetzen des Auftrags).</span><span class="sxs-lookup"><span data-stu-id="b841d-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="b841d-123">Verwalten des Bits-Übertragungs Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b841d-123">Manage the BITS transfer job.</span></span>

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    <span data-ttu-id="b841d-124">Das vorherige Beispiel ist ein Skript, mit dem der Status des Auftrags abgerufen und eine Aktion basierend auf dem Status ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b841d-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="b841d-125">Die folgenden Aktionen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="b841d-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="b841d-126">Wenn $result. Der Status ist 4 (**Fehler des BG- \_ Auftrags \_ Zustands \_**), das [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) -Cmdlet ruft die [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) -Methode auf und bricht den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="b841d-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="b841d-127">Wenn $result. Der Status ist 5 (ein **\_ \_ \_ vorübergehender \_ Fehler des BG-Auftrags Zustands**), das Cmdlet " [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) " Ruft die Methode " [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) " auf und bricht den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="b841d-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="b841d-128">Wenn $result. Der Status ist 6 (der **BG- \_ Auftrags \_ Status wurde \_ übertragen**), das Cmdlet " [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) " Ruft die [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) -Methode auf und legt den Status auf "abgeschlossen" fest</span><span class="sxs-lookup"><span data-stu-id="b841d-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="b841d-129">Weitere Informationen zu Auftrags Zuständen finden Sie unter der [**BG- \_ Auftrags \_ Status**](/windows/desktop/api/Bits/ne-bits-bg_job_state) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b841d-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b841d-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b841d-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b841d-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="b841d-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="b841d-132">"Aufrufen-wsmanaction"</span><span class="sxs-lookup"><span data-stu-id="b841d-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="b841d-133">Set-wsmaninstance</span><span class="sxs-lookup"><span data-stu-id="b841d-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 

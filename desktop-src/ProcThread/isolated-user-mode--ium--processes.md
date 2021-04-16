---
description: In Windows 10 wurde eine neue Sicherheitsfunktion mit dem Namen "Virtual Secure Mode (VSM)" eingeführt.
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Isolierte Benutzermodusprozesse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553287"
---
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="dcd36-103">Isolierte Benutzermodusprozesse</span><span class="sxs-lookup"><span data-stu-id="dcd36-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="dcd36-104">In Windows 10 wurde eine neue Sicherheitsfunktion mit dem Namen "Virtual Secure Mode (VSM)" eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dcd36-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="dcd36-105">VSM nutzt den Hyper-V-Hypervisor und den slat (Second Level Address Translation) zum Erstellen eines Satzes von Modi, die als virtuelle Vertrauens Ebenen (Virtual Trust Levels, VTLs) bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="dcd36-106">Diese neue Softwarearchitektur erstellt eine Sicherheitsgrenze, um zu verhindern, dass Prozesse, die in einer VTL ausgeführt werden, auf den Arbeitsspeicher einer anderen VTL zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="dcd36-107">Der Vorteil dieser Isolation ist die zusätzliche Entschärfung von kernelexploits beim Schutz von Assets wie Kennworthashes und Kerberos-Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="dcd36-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="dcd36-108">In Abbildung 1 wird das herkömmliche Modell für den Kernel Modus und den Benutzermoduscode dargestellt, der in CPU-Ring 0 bzw. Ring 3 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd36-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="dcd36-109">In diesem neuen Modell wird der Code, der im herkömmlichen Modell ausgeführt wird, in VTL0 ausgeführt und kann nicht auf die höheren privilegierten VTL1 zugreifen, wo der sichere Kernel und der isolierte Benutzermodus (Code) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="dcd36-110">Die VTLs sind hierarchische, d. h., Code, der in VTL1 ausgeführt wird, ist privilegierter als Code in VTL0.</span><span class="sxs-lookup"><span data-stu-id="dcd36-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="dcd36-111">Die VTL-Isolation wird vom Hyper-V-Hypervisor erstellt, der mithilfe der Second Level Address Translation (slat) Speicher zum Startzeitpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="dcd36-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="dcd36-112">Dies wird dynamisch fortgesetzt, wenn das System ausgeführt wird, und der Arbeitsspeicher schützt den sicheren Kernel, der den Schutz von VTL0 angibt, da er zum enthalten geheimer Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcd36-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="dcd36-113">Da separate Speicherblöcke für die beiden VTLs zugewiesen werden, wird eine sichere Laufzeitumgebung für VTL1 erstellt, indem den VTL1 und VTL0 exklusive Speicherblöcke mit den entsprechenden Zugriffsberechtigungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="dcd36-114">**Diagramm 1-Architektur des-IUMS**</span><span class="sxs-lookup"><span data-stu-id="dcd36-114">**Diagram 1 - IUM Architecture**</span></span>

![Diagramm 1-Architektur des-IUMS](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="dcd36-116">Trust Lets</span><span class="sxs-lookup"><span data-stu-id="dcd36-116">Trustlets</span></span>

<span data-ttu-id="dcd36-117">Trust Lets (auch als vertrauenswürdige Prozesse, sichere Prozesse oder ium-Prozesse bezeichnet) sind Programme, die als IOT-Prozesse in VSM ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="dcd36-118">Sie vervollständigen Systemaufrufe, indem Sie Sie an den Windows-Kernel Marshalling, der in VTL0 Ring 0 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd36-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="dcd36-119">VSM erstellt eine kleine Ausführungsumgebung, die den kleinen sicheren Kernel umfasst, der in VTL1 ausgeführt wird (isoliert von dem Kernel und den Treibern, die in VTL0 ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="dcd36-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="dcd36-120">Der eindeutige Sicherheitsvorteil ist die Isolation von Trust Let-Benutzermodus-Seiten in VTL1 von Treibern, die im VTL0-Kernel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="dcd36-121">Auch wenn der Kernel Modus von VTL0 durch Schadsoftware kompromittiert wird, hat er keinen Zugriff auf die Arbeitsseiten des Arbeitsprozesses.</span><span class="sxs-lookup"><span data-stu-id="dcd36-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="dcd36-122">Wenn VSM aktiviert ist, wird die LSASS-Umgebung (Local Security Authority, lokale Sicherheits Autorität) als Trust-Let ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcd36-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="dcd36-123">LSASS verwaltet die Richtlinie des lokalen Systems, die Benutzerauthentifizierung und die Überwachung bei der Behandlung von sensiblen Sicherheitsdaten, z. b. Kennworthashes und Kerberos-Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="dcd36-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="dcd36-124">Um die Sicherheitsvorteile von VSM zu nutzen, wird ein vertrauenswürdiges mit dem Namen "LSAISO.exe (LSA isoliert)" in VTL1 ausgeführt und kommuniziert mit LSASS.exe, die in VTL0 über einen RPC-Kanal ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="dcd36-125">Die lsaiso-Geheimnisse werden verschlüsselt, bevor Sie an den LSASS gesendet werden, der im normalen VSM-Modus ausgeführt wird, und die lsaiso-Seiten werden vor bösartigem Code in VTL0 geschützt.</span><span class="sxs-lookup"><span data-stu-id="dcd36-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="dcd36-126">**Diagramm 2 – LSASS Trust Let Design**</span><span class="sxs-lookup"><span data-stu-id="dcd36-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="dcd36-127">Diagramm 2 – LSASS Trust Let Design</span><span class="sxs-lookup"><span data-stu-id="dcd36-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="dcd36-128">Auswirkungen des isolierten Benutzermodus (IUM)</span><span class="sxs-lookup"><span data-stu-id="dcd36-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="dcd36-129">Es ist nicht möglich, an einen ium-Prozess anzufügen, was die Möglichkeit zum Debuggen von VTL1-Code hemmt.</span><span class="sxs-lookup"><span data-stu-id="dcd36-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="dcd36-130">Dies umfasst das nach dem Debuggen von Speicher Abbildern und das Anfügen der Debugtools für das Live Debuggen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="dcd36-131">Es umfasst auch Versuche von privilegierten Konten oder Kernel Treibern, um eine DLL in einen ium-Prozess zu laden, einen Thread einzufügen oder ein APC im Benutzermodus bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="dcd36-132">Derartige Versuche können zur Destabilisierung des gesamten Systems führen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="dcd36-133">Windows-APIs, die die Sicherheit eines trustlets beeinträchtigen würden, können auf unerwartete Weise fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="dcd36-134">Wenn Sie z. b. eine DLL in ein vertrauenswürdiges laden, wird Sie in VTL0, aber nicht in VTL1 verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="dcd36-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="dcd36-135">Queueuserapc schlägt möglicherweise automatisch fehl, wenn sich der Zielthread in einem Trust-Trust-Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="dcd36-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="dcd36-136">Andere APIs, wie z. b. "kreateremotethread", "virtualbelegcex" und "Read/Write-processmemory", funktionieren ebenfalls nicht wie erwartet, wenn Sie für trustlets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd36-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="dcd36-137">Verwenden Sie den unten stehenden Beispielcode, um zu verhindern, dass Funktionen aufgerufen werden, die versuchen, Code an einen-Prozess anzufügen oder einzufügen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="dcd36-138">Dies schließt Kernel Treiber ein, die APCs für die Ausführung von Code in einem trustlet in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="dcd36-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd36-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcd36-139">Remarks</span></span>

<span data-ttu-id="dcd36-140">Wenn der Rückgabestatus von issecureprocess Erfolg ist, überprüfen Sie den secureprocess \_ out- \_ Parameter, um zu bestimmen, ob der Prozess ein ium-Prozess ist.</span><span class="sxs-lookup"><span data-stu-id="dcd36-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="dcd36-141">IUM-Prozesse werden durch das System als "sichere Prozesse" gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="dcd36-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="dcd36-142">Ein boolesches Ergebnis von "true" bedeutet, dass der Ziel Prozess den Typ "ium" hat.</span><span class="sxs-lookup"><span data-stu-id="dcd36-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



<span data-ttu-id="dcd36-143">Das WDK für Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", enthält die erforderliche Definition der \_ erweiterten \_ grundlegenden \_ Informationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="dcd36-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="dcd36-144">Die aktualisierte Version der Struktur wird in "ntddk. h" mit dem neuen Feld "issecureprocess" definiert.</span><span class="sxs-lookup"><span data-stu-id="dcd36-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 




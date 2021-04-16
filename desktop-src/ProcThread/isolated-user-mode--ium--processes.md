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
# <a name="isolated-user-mode-ium-processes"></a>Isolierte Benutzermodusprozesse

In Windows 10 wurde eine neue Sicherheitsfunktion mit dem Namen "Virtual Secure Mode (VSM)" eingeführt. VSM nutzt den Hyper-V-Hypervisor und den slat (Second Level Address Translation) zum Erstellen eines Satzes von Modi, die als virtuelle Vertrauens Ebenen (Virtual Trust Levels, VTLs) bezeichnet werden. Diese neue Softwarearchitektur erstellt eine Sicherheitsgrenze, um zu verhindern, dass Prozesse, die in einer VTL ausgeführt werden, auf den Arbeitsspeicher einer anderen VTL zugreifen. Der Vorteil dieser Isolation ist die zusätzliche Entschärfung von kernelexploits beim Schutz von Assets wie Kennworthashes und Kerberos-Schlüsseln.

In Abbildung 1 wird das herkömmliche Modell für den Kernel Modus und den Benutzermoduscode dargestellt, der in CPU-Ring 0 bzw. Ring 3 ausgeführt wird. In diesem neuen Modell wird der Code, der im herkömmlichen Modell ausgeführt wird, in VTL0 ausgeführt und kann nicht auf die höheren privilegierten VTL1 zugreifen, wo der sichere Kernel und der isolierte Benutzermodus (Code) ausgeführt werden. Die VTLs sind hierarchische, d. h., Code, der in VTL1 ausgeführt wird, ist privilegierter als Code in VTL0.

Die VTL-Isolation wird vom Hyper-V-Hypervisor erstellt, der mithilfe der Second Level Address Translation (slat) Speicher zum Startzeitpunkt zuweist. Dies wird dynamisch fortgesetzt, wenn das System ausgeführt wird, und der Arbeitsspeicher schützt den sicheren Kernel, der den Schutz von VTL0 angibt, da er zum enthalten geheimer Schlüssel verwendet wird. Da separate Speicherblöcke für die beiden VTLs zugewiesen werden, wird eine sichere Laufzeitumgebung für VTL1 erstellt, indem den VTL1 und VTL0 exklusive Speicherblöcke mit den entsprechenden Zugriffsberechtigungen zugewiesen werden.

**Diagramm 1-Architektur des-IUMS**

![Diagramm 1-Architektur des-IUMS](images/uim-architecture.png)

## <a name="trustlets"></a>Trust Lets

Trust Lets (auch als vertrauenswürdige Prozesse, sichere Prozesse oder ium-Prozesse bezeichnet) sind Programme, die als IOT-Prozesse in VSM ausgeführt werden. Sie vervollständigen Systemaufrufe, indem Sie Sie an den Windows-Kernel Marshalling, der in VTL0 Ring 0 ausgeführt wird. VSM erstellt eine kleine Ausführungsumgebung, die den kleinen sicheren Kernel umfasst, der in VTL1 ausgeführt wird (isoliert von dem Kernel und den Treibern, die in VTL0 ausgeführt werden). Der eindeutige Sicherheitsvorteil ist die Isolation von Trust Let-Benutzermodus-Seiten in VTL1 von Treibern, die im VTL0-Kernel ausgeführt werden. Auch wenn der Kernel Modus von VTL0 durch Schadsoftware kompromittiert wird, hat er keinen Zugriff auf die Arbeitsseiten des Arbeitsprozesses.

Wenn VSM aktiviert ist, wird die LSASS-Umgebung (Local Security Authority, lokale Sicherheits Autorität) als Trust-Let ausgeführt. LSASS verwaltet die Richtlinie des lokalen Systems, die Benutzerauthentifizierung und die Überwachung bei der Behandlung von sensiblen Sicherheitsdaten, z. b. Kennworthashes und Kerberos-Schlüsseln. Um die Sicherheitsvorteile von VSM zu nutzen, wird ein vertrauenswürdiges mit dem Namen "LSAISO.exe (LSA isoliert)" in VTL1 ausgeführt und kommuniziert mit LSASS.exe, die in VTL0 über einen RPC-Kanal ausgeführt werden. Die lsaiso-Geheimnisse werden verschlüsselt, bevor Sie an den LSASS gesendet werden, der im normalen VSM-Modus ausgeführt wird, und die lsaiso-Seiten werden vor bösartigem Code in VTL0 geschützt.

**Diagramm 2 – LSASS Trust Let Design**

![Diagramm 2 – LSASS Trust Let Design ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Auswirkungen des isolierten Benutzermodus (IUM)

Es ist nicht möglich, an einen ium-Prozess anzufügen, was die Möglichkeit zum Debuggen von VTL1-Code hemmt. Dies umfasst das nach dem Debuggen von Speicher Abbildern und das Anfügen der Debugtools für das Live Debuggen. Es umfasst auch Versuche von privilegierten Konten oder Kernel Treibern, um eine DLL in einen ium-Prozess zu laden, einen Thread einzufügen oder ein APC im Benutzermodus bereitzustellen. Derartige Versuche können zur Destabilisierung des gesamten Systems führen. Windows-APIs, die die Sicherheit eines trustlets beeinträchtigen würden, können auf unerwartete Weise fehlschlagen. Wenn Sie z. b. eine DLL in ein vertrauenswürdiges laden, wird Sie in VTL0, aber nicht in VTL1 verfügbar gemacht. Queueuserapc schlägt möglicherweise automatisch fehl, wenn sich der Zielthread in einem Trust-Trust-Gerät befindet. Andere APIs, wie z. b. "kreateremotethread", "virtualbelegcex" und "Read/Write-processmemory", funktionieren ebenfalls nicht wie erwartet, wenn Sie für trustlets verwendet werden.

Verwenden Sie den unten stehenden Beispielcode, um zu verhindern, dass Funktionen aufgerufen werden, die versuchen, Code an einen-Prozess anzufügen oder einzufügen. Dies schließt Kernel Treiber ein, die APCs für die Ausführung von Code in einem trustlet in die Warteschlange stellen.

## <a name="remarks"></a>Bemerkungen

Wenn der Rückgabestatus von issecureprocess Erfolg ist, überprüfen Sie den secureprocess \_ out- \_ Parameter, um zu bestimmen, ob der Prozess ein ium-Prozess ist. IUM-Prozesse werden durch das System als "sichere Prozesse" gekennzeichnet. Ein boolesches Ergebnis von "true" bedeutet, dass der Ziel Prozess den Typ "ium" hat.


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



Das WDK für Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", enthält die erforderliche Definition der \_ erweiterten \_ grundlegenden \_ Informationsstruktur. Die aktualisierte Version der Struktur wird in "ntddk. h" mit dem neuen Feld "issecureprocess" definiert.


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



 

 




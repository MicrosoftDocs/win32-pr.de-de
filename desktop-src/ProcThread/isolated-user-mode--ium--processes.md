---
description: Windows 10 ein neues Sicherheitsfeature namens Virtual Secure Mode (VSM) eingeführt.
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Isolierte Benutzermodusprozesse (Isolated User Mode, IUM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982d9924f60d02a74aa7237e5c3bb16e787f1d3a0cc07e9693e9cd47335cedc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032539"
---
# <a name="isolated-user-mode-ium-processes"></a>Isolierte Benutzermodusprozesse (Isolated User Mode, IUM)

Windows 10 ein neues Sicherheitsfeature namens Virtual Secure Mode (VSM) eingeführt. VSM nutzt den Hyper-V-Hypervisor und die Adressübersetzung der zweiten Ebene (Second Level Address Translation, SLAT), um einen Satz von Modi zu erstellen, die als virtuelle Vertrauensebenen (Virtual Trust Levels, VTLs) bezeichnet werden. Diese neue Softwarearchitektur erstellt eine Sicherheitsgrenze, um zu verhindern, dass prozesse, die in einer VTL ausgeführt werden, auf den Arbeitsspeicher einer anderen VTL zugreifen. Der Vorteil dieser Isolation schließt eine zusätzliche Entschärfung von Kernel-Exploits ein, während Ressourcen wie Kennworthashes und Kerberos-Schlüssel geschützt werden.

Abbildung 1 zeigt das herkömmliche Modell des Kernelmodus- bzw. Benutzermoduscodes, der in CPU-Ring 0 bzw. Ring 3 ausgeführt wird. In diesem neuen Modell wird der im herkömmlichen Modell ausgeführte Code in VTL0 ausgeführt und kann nicht auf die VTL1 mit höheren Berechtigungen zugreifen, bei der der sichere Kernel und der isolierte Benutzermodus (IUM) Code ausführen. Die VTLs sind hierarchisch, was bedeutet, dass jeder code, der in VTL1 ausgeführt wird, privilegierter ist als Code, der in VTL0 ausgeführt wird.

Die VTL-Isolation wird vom Hyper-V-Hypervisor erstellt, der arbeitsspeicherbasierten Speicher mithilfe der Adressübersetzung der zweiten Ebene (Second Level Address Translation, SLAT) zuordnt. Dies wird dynamisch fortgesetzt, während das System ausgeführt wird, um den Arbeitsspeicher zu schützen, der vom sicheren Kernel angegeben wird, dass Schutz vor VTL0 benötigt wird, da er zum Enthalten von Geheimnissen verwendet wird. Da den beiden VTLs separate Speicherblöcke zugeordnet werden, wird eine sichere Laufzeitumgebung für VTL1 erstellt, indem exklusive Speicherblöcke VTL1 und VTL0 mit den entsprechenden Zugriffsberechtigungen zugewiesen werden.

**Diagramm 1: IUM-Architektur**

![Diagramm 1 – ium-Architektur](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Trustlets (auch als vertrauenswürdige Prozesse, sichere Prozesse oder IUM-Prozesse bezeichnet) sind Programme, die als IUM-Prozesse in VSM ausgeführt werden. Sie schließen Systemaufrufe ab, indem sie sie zum Windows Kernel marshallen, der in VTL0 Ring 0 ausgeführt wird. VSM erstellt eine kleine Ausführungsumgebung, die den kleinen sicheren Kernel enthält, der in VTL1 ausgeführt wird (isoliert vom Kernel und treibern, die in VTL0 ausgeführt werden). Der eindeutige Sicherheitsvorteil ist die Isolation von Trustlet-Benutzermodusseiten in VTL1 von Treibern, die im VTL0-Kernel ausgeführt werden. Auch wenn der Kernelmodus von VTL0 durch Schadsoftware kompromittiert wird, hat er keinen Zugriff auf die IUM-Prozessseiten.

Wenn VSM aktiviert ist, wird die Umgebung der lokalen Sicherheitsstelle (Local Security Authority, LSASS) als Trustlet ausgeführt. LSASS verwaltet die lokale Systemrichtlinie, Benutzerauthentifizierung und Überwachung, während vertrauliche Sicherheitsdaten wie Kennworthashes und Kerberos-Schlüssel verwaltet werden. Um die Sicherheitsvorteile von VSM zu nutzen, wird ein Trustlet namens LSAISO.exe (LSA Isolated) in VTL1 ausgeführt und kommuniziert über einen RPC-Kanal mit LSASS.exe, das in VTL0 ausgeführt wird. Die LSAISO-Geheimnisse werden verschlüsselt, bevor sie an LSASS übertragen werden, die im normalen VSM-Modus ausgeführt werden, und die Seiten von LSAISO sind vor schädlichem Code geschützt, der in VTL0 ausgeführt wird.

**Diagramm 2 – LSASS Trustlet-Entwurf**

![Diagramm 2 – lsass trustlet-Entwurf ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Auswirkungen des isolierten Benutzermodus (Isolated User Mode, IUM)

Es ist nicht möglich, an einen IUM-Prozess angefügt zu werden, was die Möglichkeit zum Debuggen von VTL1-Code verhindert. Dies schließt das Post-Dump-Debuggen von Speicherabbilds und das Anfügen der Debugtools für das Livedebuggen ein. Sie umfasst auch Versuche von privilegierten Konten oder Kerneltreibern, eine DLL in einen IUM-Prozess zu laden, einen Thread einzujizieren oder einen Benutzermodus-APC zu liefern. Solche Versuche können zu einer Destabilisierung des gesamten Systems führen. Windows APIs, die die Sicherheit eines Trustlet gefährden würden, können auf unerwartete Weise fehlschlagen. Wenn Sie beispielsweise eine DLL in ein Trustlet laden, wird sie in VTL0, aber nicht in VTL1 verfügbar gemacht. QueueUserApc kann im Hintergrund fehlschlagen, wenn sich der Zielthread in einem Trustlet befindet. Andere APIs wie CreateRemoteThread, VirtualAllocEx und Read/WriteProcessMemory funktionieren auch nicht wie erwartet, wenn sie für Trustlets verwendet werden.

Verwenden Sie den folgenden Beispielcode, um das Aufrufen von Funktionen zu verhindern, die versuchen, Code an einen IUM-Prozess anfügen oder in einen IUM-Prozess einfügen. Dies schließt Kerneltreiber ein, die APCs für die Ausführung von Code in einem Trustlet in die Warteschlange stellen.

## <a name="remarks"></a>Hinweise

Wenn der Rückgabestatus von IsSecureProcess erfolgreich ist, überprüfen Sie den SecureProcess Out-Parameter, um zu ermitteln, ob der Prozess ein \_ \_ IUM-Prozess ist. IUM-Prozesse werden vom System als "Sichere Prozesse" gekennzeichnet. Ein boolesches Ergebnis von TRUE bedeutet, dass der Zielprozess vom Typ IUM ist.


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



Das WDK für Windows 10, "Windows Driver Kit – Windows 10.0.15063.0", enthält die erforderliche Definition der PROCESS \_ EXTENDED \_ BASIC \_ INFORMATION-Struktur. Die aktualisierte Version der -Struktur wird in ntddk.h mit dem neuen Feld IsSecureProcess definiert.


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



 

 




---
description: Ein Zugriffsrecht ist ein Bitflag, das einem bestimmten Satz von Vorgängen entspricht, die ein Thread für ein sicherungsfähiges Objekt ausführen kann.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Zugriffsrechte und Zugriffsmasken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1238766e2e4c8629b6c3a508b30d1e8832314d2e8ddd5ffdf4a1b93085f3c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914357"
---
# <a name="access-rights-and-access-masks"></a>Zugriffsrechte und Zugriffsmasken

Ein *Zugriffsrecht ist* ein Bitflag, das einem bestimmten Satz von Vorgängen entspricht, die ein Thread für ein sicherungsfähiges Objekt ausführen kann. Beispielsweise verfügt ein Registrierungsschlüssel über das Zugriffsrecht KEY SET VALUE, das der Fähigkeit eines Threads entspricht, einen Wert unter dem \_ \_ Schlüssel zu setzen. Wenn ein Thread versucht, einen Vorgang für ein Objekt durchzuführen, aber nicht über das erforderliche Zugriffsrecht auf das Objekt verfügt, führt das System den Vorgang nicht aus.

Eine [*Zugriffsmaske*](/windows/desktop/SecGloss/a-gly) ist ein 32-Bit-Wert, dessen Bits den von einem -Objekt unterstützten Zugriffsrechten entsprechen. Alle Windows sicherungsfähige Objekte verwenden ein [Zugriffsmaskenformat,](access-mask-format.md) das Bits für die folgenden Zugriffsberechtigungstypen enthält:

-   [Generische Zugriffsrechte](generic-access-rights.md)
-   [Standardzugriffsrechte](standard-access-rights.md)
-   [SACL-Zugriffsrecht](sacl-access-right.md)
-   [Zugriffsrechte für Verzeichnisdienste](directory-services-access-rights.md)

Wenn ein Thread versucht, ein Handle für ein Objekt zu öffnen, gibt der Thread in der Regel eine Zugriffsmaske an, um einen Satz [von Zugriffsrechten an fordern zu können.](requesting-access-rights-to-an-object.md) Beispielsweise kann eine Anwendung, die die Werte eines Registrierungsschlüssels festlegen und abfragen muss, den Schlüssel mithilfe einer Zugriffsmaske öffnen, um die Zugriffsrechte KEY SET VALUE und \_ KEY QUERY VALUE an \_ \_ \_ fordern.

Die folgende Tabelle zeigt die Funktionen, die die Sicherheitsinformationen für jeden Typ von sicherungsfähigem Objekt bearbeiten.



| Objekttyp                                                                                                                                           | Sicherheitsdeskriptorfunktionen                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateien oder Verzeichnisse in](/windows/desktop/FileIO/file-security-and-access-rights) einem NTFS-Dateisystem                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Named Pipes](/windows/desktop/ipc/named-pipe-security-and-access-rights)[Anonymous Pipes](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Konsolenbildschirmpuffer                                                                                                                                | Wird nicht unterstützt.                                                                                                                                                                                     |
| [Prozessthreads](/windows/desktop/ProcThread/process-security-and-access-rights)[](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Dateizuordnungsobjekte](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Zugriffstoken](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Fensterverwaltungsobjekte ([Fensterstationen](/windows/desktop/winstation/window-station-security-and-access-rights) und [Desktops](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows-Dienste](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Lokale Drucker oder Remotedrucker                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Netzwerkfreigaben                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Prozessübergreifende Synchronisierungsobjekte](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (Ereignisse, Mutexe, Semaphore und wartebare Timer)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Auftragsobjekte](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 


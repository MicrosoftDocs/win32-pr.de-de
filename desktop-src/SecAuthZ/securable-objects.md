---
description: Ein sicherungsfähiges Objekt ist ein Objekt, das über einen Sicherheitsdeskriptor verfügen kann.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Sicherungsfähige Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93af0153082a5e94577e96e3b3f85c30ced8775aa8617bff84db37c96904d814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780505"
---
# <a name="securable-objects"></a>Sicherungsfähige Objekte

Ein sicherungsfähiges Objekt ist ein Objekt, das über einen [Sicherheitsdeskriptor verfügen kann.](security-descriptors.md) Alle benannten Windows sind sicherungsfähig. Einige unbenannte Objekte, z. B. [*Prozess-*](/windows/desktop/SecGloss/p-gly) und Threadobjekte, können auch Sicherheitsdeskriptoren aufweisen. Für die meisten sicherungsfähige Objekte können [](/windows/desktop/SecGloss/s-gly) Sie den Sicherheitsdeskriptor eines Objekts im Funktionsaufruf angeben, der das Objekt erstellt. Beispielsweise können Sie einen Sicherheitsdeskriptor in den [**Funktionen CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) und [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) angeben.

Darüber hinaus ermöglichen Windows Sicherheitsfunktionen das Erhalten und Festlegen der Sicherheitsinformationen für sicherungsfähige Objekte, die auf anderen Betriebssystemen als Windows. Die Windows Sicherheitsfunktionen bieten auch Unterstützung für die Verwendung von Sicherheitsbeschreibungen mit privaten, anwendungsdefinierten Objekten. Weitere Informationen zu privaten sicherungsfähige Objekte finden Sie unter [Client/Server Access Control](client-server-access-control.md).

Jeder Typ von sicherungsfähigem Objekt [](access-rights-and-access-masks.md) definiert einen eigenen Satz spezifischer Zugriffsrechte und seine eigene [Zuordnung generischer Zugriffsrechte.](generic-access-rights.md) Informationen zu den spezifischen und generischen Zugriffsrechten für jeden Typ von sicherungsfähigem Objekt finden Sie in der Übersicht für diesen Objekttyp.

Die folgende Tabelle zeigt die Funktionen, die zum Bearbeiten der Sicherheitsinformationen für einige allgemeine sicherungsfähige Objekte verwendet werden können.



| Objekttyp                                                                                                                                           | Sicherheitsdeskriptorfunktionen                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateien oder Verzeichnisse in](/windows/desktop/FileIO/file-security-and-access-rights) einem NTFS-Dateisystem                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Named Pipes](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Anonyme Pipes](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Prozesse](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Dateizuordnungsobjekte](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Zugriffstoken](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Fensterverwaltungsobjekte ([Fensterstationen](/windows/desktop/winstation/window-station-security-and-access-rights) und [Desktops](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows-Dienste](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Lokale Drucker oder Remotedrucker                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Netzwerkfreigaben                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Prozessübergreifende Synchronisierungsobjekte](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (Ereignisse, Mutexe, Semaphore und wartebare Timer)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Auftragsobjekte](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Verzeichnisdienstobjekte                                                                                                                             | Diese Objekte werden von Active Directory-Objekten verarbeitet. Weitere Informationen finden Sie unter [Active Directory-Dienstschnittstellen.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)                             |



 

 


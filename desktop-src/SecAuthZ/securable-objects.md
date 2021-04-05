---
description: Ein Sicherungs fähiges Objekt ist ein Objekt, das über eine Sicherheits Beschreibung verfügen kann.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Sicherungs fähige Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867a40e781d9d7f97302ed6e592a7fc26d61b939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752752"
---
# <a name="securable-objects"></a>Sicherungs fähige Objekte

Ein Sicherungs fähiges Objekt ist ein Objekt, das über eine [Sicherheits Beschreibung](security-descriptors.md)verfügen kann. Alle benannten Windows-Objekte sind Sicherungs fähig. Einige unbenannte Objekte (z. b. [*Prozess*](/windows/desktop/SecGloss/p-gly) -und Thread Objekte) können auch Sicherheits Deskriptoren aufweisen. Bei den meisten Sicherungs fähigen Objekten können Sie die [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) eines Objekts im Funktionsaufruf angeben, von dem das Objekt erstellt wird. Sie können z. b. eine Sicherheits Beschreibung [**in den Funktionen**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "up" und " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " angeben.

Darüber hinaus können Sie mit den Windows-Sicherheitsfunktionen die Sicherheitsinformationen für Sicherungs fähige Objekte, die auf anderen Betriebssystemen als Windows erstellt werden, erhalten und festlegen. Die Windows-Sicherheitsfunktionen bieten auch Unterstützung für die Verwendung von Sicherheits Deskriptoren mit privaten, Anwendungs definierten Objekten. Weitere Informationen zu privaten Sicherungs fähigen Objekten finden Sie unter [Client/Server Access Control](client-server-access-control.md).

Jeder Typ eines Sicherungs fähigen Objekts definiert seinen eigenen Satz spezifischer [Zugriffsrechte](access-rights-and-access-masks.md) und seine eigene [Zuordnung generischer Zugriffsrechte](generic-access-rights.md). Informationen zu den spezifischen und generischen Zugriffsrechten für die einzelnen Typen von Sicherungs fähigen Objekten finden Sie in der Übersicht für diesen Objekttyp.

In der folgenden Tabelle sind die Funktionen aufgeführt, die zum Bearbeiten der Sicherheitsinformationen für einige gängige Sicherungs fähige Objekte verwendet werden.



| Objekttyp                                                                                                                                           | Sicherheitsbeschreibungerfunktionen                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateien oder Verzeichnisse](/windows/desktop/FileIO/file-security-and-access-rights) in einem NTFS-Dateisystem                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Named Pipes](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Anonyme Pipes](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Prozesse](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Datei Zuordnung von Objekten](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Zugriffstoken](access-rights-for-access-token-objects.md)                                                                                           | [**Setkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **getkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Fenster Verwaltungs Objekte ([Fenster Stationen](/windows/desktop/winstation/window-station-security-and-access-rights) und [Desktops](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows-Dienste](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Lokale oder Remote Drucker                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Netzwerkfreigaben                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Prozessübergreifende Synchronisierungs Objekte](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (Ereignisse, Mutexen, Semaphore und aufnutzbare Timer)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Auftrags Objekte](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Verzeichnisdienst Objekte                                                                                                                             | Diese Objekte werden von Active Directory-Objekten behandelt. Weitere Informationen finden Sie unter [Active Directory-Dienst Schnittstellen](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).                             |



 

 


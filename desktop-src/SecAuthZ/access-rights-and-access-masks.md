---
description: Ein Zugriffsrecht ist ein Bitflag, das einem bestimmten Satz von Vorgängen entspricht, die ein Thread für ein Sicherungs fähiges Objekt ausführen kann.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Zugriffsrechte und Zugriffs Masken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f06cdf447f9d91c1553ea5fb6b3b7d1f324dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393657"
---
# <a name="access-rights-and-access-masks"></a>Zugriffsrechte und Zugriffs Masken

Ein *Zugriffsrecht* ist ein Bitflag, das einem bestimmten Satz von Vorgängen entspricht, die ein Thread für ein Sicherungs fähiges Objekt ausführen kann. Beispielsweise verfügt ein Registrierungsschlüssel über das Zugriffsrecht für den Schlüssel \_ Satz \_ Wert, der der Fähigkeit eines Threads entspricht, einen Wert unter dem Schlüssel festzulegen. Wenn ein Thread versucht, einen Vorgang für ein Objekt auszuführen, jedoch nicht über die erforderlichen Zugriffsrechte für das Objekt verfügt, führt das System den Vorgang nicht aus.

Eine [*Zugriffs Maske*](/windows/desktop/SecGloss/a-gly) ist ein 32-Bit-Wert, dessen Bits den von einem-Objekt unterstützten Zugriffsrechten entspricht. Alle Sicherungs fähigen Windows-Objekte verwenden ein [Zugriffs Masken Format](access-mask-format.md) , das Bits für die folgenden Typen von Zugriffsrechten umfasst:

-   [Generische Zugriffsrechte](generic-access-rights.md)
-   [Standard Zugriffsrechte](standard-access-rights.md)
-   [SACL-Zugriffsrecht](sacl-access-right.md)
-   [Zugriffsrechte für Verzeichnisdienste](directory-services-access-rights.md)

Wenn ein Thread versucht, ein Handle für ein Objekt zu öffnen, gibt der Thread in der Regel eine Zugriffs Maske zum [Anfordern eines Satzes von Zugriffsrechten](requesting-access-rights-to-an-object.md)an. Beispielsweise kann eine Anwendung, die die Werte eines Registrierungsschlüssels festlegen und Abfragen muss, den Schlüssel mithilfe einer Zugriffs Maske öffnen, um den Schlüssel \_ Satz \_ Wert und die \_ Zugriffsrechte für Schlüssel Abfrage \_ Werte anzufordern.

In der folgenden Tabelle sind die Funktionen aufgeführt, mit denen die Sicherheitsinformationen für die einzelnen Typen von Sicherungs fähigen Objekten geändert werden.



| Objekttyp                                                                                                                                           | Sicherheitsbeschreibungerfunktionen                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateien oder Verzeichnisse](/windows/desktop/FileIO/file-security-and-access-rights) in einem NTFS-Dateisystem                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Anonyme](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights) Pipes mit [Named Pipes](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Konsolenbildschirm Puffer                                                                                                                                | Wird nicht unterstützt.                                                                                                                                                                                     |
| [Verarbeitet](/windows/desktop/ProcThread/process-security-and-access-rights)[Threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Datei Zuordnung von Objekten](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Zugriffstoken](access-rights-for-access-token-objects.md)                                                                                           | [**Setkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **getkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Fenster Verwaltungs Objekte ([Fenster Stationen](/windows/desktop/winstation/window-station-security-and-access-rights) und [Desktops](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows-Dienste](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Lokale oder Remote Drucker                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Netzwerkfreigaben                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Prozessübergreifende Synchronisierungs Objekte](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (Ereignisse, Mutexen, Semaphore und aufnutzbare Timer)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Auftrags Objekte](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 


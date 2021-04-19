---
description: Das Windows-Sicherheitsmodell ermöglicht es Ihnen, den Zugriff auf Ereignis-, Mutex-, Semaphore-und wabbare Timer-Objekte zu steuern. Zeit Geber Warteschlangen, Interlocked-Variablen und kritische Abschnitts Objekte können nicht Sicherungs fähig sein. Weitere Informationen finden Sie unter Access-Control Modell.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c4bfdb17a6e1c4d99a3e9722e67a3b48a3c788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357790"
---
# <a name="synchronization-object-security-and-access-rights"></a>Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt

Das Windows-Sicherheitsmodell ermöglicht es Ihnen, den Zugriff auf Ereignis-, Mutex-, Semaphore-und wabbare Timer-Objekte zu steuern. Zeit Geber Warteschlangen, Interlocked-Variablen und kritische Abschnitts Objekte können nicht Sicherungs fähig sein. Weitere Informationen finden Sie unter [Zugriffs Steuerungsmodell](../secauthz/access-control-model.md).

Sie können eine [Sicherheits Beschreibung](../secauthz/security-descriptors.md) für ein Prozess Objekt für die prozessübergreifende Synchronisierung angeben, wenn Sie die Funktion "up- [**Event**](/windows/win32/api/synchapi/nf-synchapi-createeventa)", " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)", " [**kreatesemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)" oder "anitatewaitabletimer" aufrufen. [](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Wenn Sie **null** angeben, erhält das Objekt eine Standard Sicherheits Beschreibung. Die [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](../secauthz/access-control-lists.md) in der Standard Sicherheits Beschreibung für ein Synchronisierungs Objekt stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.

Zum Abrufen oder Festlegen der Sicherheits Beschreibung eines Ereignisses, Mutex, Semaphors oder eines ausnutzbaren timerobjekts aufrufen Sie die Funktionen [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)oder [**setsecurityinfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Die von " [**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)", " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)", " [**kreatesemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)" und " [**kreatewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) " zurückgegebenen Handles haben vollen Zugriff auf das neue Objekt. Wenn Sie die Funktionen [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**opensemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)und [**openwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) aufrufen, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Objekts.

Die gültigen Zugriffsrechte für die prozessübergreifenden Synchronisierungs Objekte umfassen die [Standard Zugriffsrechte](../secauthz/standard-access-rights.md) und einige objektspezifische Zugriffsrechte. In der folgenden Tabelle sind die standardmäßigen Zugriffsrechte aufgelistet, die von allen Objekten verwendet werden.

| Wert                           | Bedeutung                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Delete** (0x00010000l)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                           |
| **Lesen Sie \_ Control** (0x00020000l) | Ist erforderlich, um Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen. Um die SACL zu lesen oder zu schreiben, müssen Sie das **Zugriffs \_ System- \_ Sicherheits** Zugriffsrecht anfordern. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](../secauthz/sacl-access-right.md). |
| **Synchronisieren** (0x00100000l)   | Das Recht, das Objekt für die Synchronisierung zu verwenden. Dadurch kann ein Thread warten, bis sich das Objekt im signalisierten Zustand befindet.                                                                                                                                                                |
| **Schreiben \_ DAC** (0x00040000l)    | Erforderlich, um die DACL in der Sicherheits Beschreibung für das-Objekt zu ändern.                                                                                                                                                                                                                   |
| **Schreiben \_ Besitzer** (0x00080000l)  | Erforderlich, um den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.                                                                                                                                                                                                                  |



 

In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte für Ereignis Objekte aufgeführt. Diese Rechte werden zusätzlich zu den Standard Zugriffsrechten unterstützt.



| Wert                             | Bedeutung                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Sämtlicher \_ Zugriff** (0x1F 0003) | Alle möglichen Zugriffsrechte für ein Ereignis Objekt. Verwenden Sie dieses Recht nur, wenn die Anwendung über den standardmäßigen Zugriffsrechte und den **Ereignis Änderungs \_ \_ Status** hinaus Zugriff erfordert. Die Verwendung dieses Zugriffsrechts erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **Ereignis \_ \_Zustand ändern** (0x0002) | Ändern des Zustands Zugriffs, der [**für die Funktionen "Server Event"**](/windows/win32/api/synchapi/nf-synchapi-setevent), " [**resettevent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) " und " [**pulsetevent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) " erforderlich ist.                                                                                                                                    |



 

In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte für Mutex-Objekte aufgeführt. Diese Rechte werden zusätzlich zu den Standard Zugriffsrechten unterstützt.



| Wert                             | Bedeutung                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mutex \_ Sämtlicher \_ Zugriff** (0x1F 0001) | Alle möglichen Zugriffsrechte für ein Mutex-Objekt. Verwenden Sie dieses Recht nur, wenn die Anwendung über die Berechtigungen hinaus zugreift, die von den Standard Zugriffsrechten gewährt werden. Die Verwendung dieses Zugriffsrechts erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **Mutex \_ \_Zustand ändern** (0x0001) | Für die zukünftige Verwendung reserviert.                                                                                                                                                                                                                                           |



 

In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte für Semaphor-Objekte aufgelistet. Diese Rechte werden zusätzlich zu den Standard Zugriffsrechten unterstützt.



| Wert                                 | Bedeutung                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Semaphore \_ Sämtlicher \_ Zugriff** (0x1F 0003) | Alle möglichen Zugriffsrechte für ein Semaphor-Objekt. Verwenden Sie dieses Recht nur, wenn die Anwendung über den Standard Zugriffsrechte und den **Semaphore-Änderungs \_ \_ Status** hinaus Zugriff benötigt. Die Verwendung dieses Zugriffsrechts erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **Semaphore \_ \_Zustand ändern** (0x0002) | Ändern des Zustands Zugriffs, der für die [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) -Funktion erforderlich ist.                                                                                                                                                                                                   |



 

In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte für aufnutzbare Timer-Objekte aufgelistet. Diese Rechte werden zusätzlich zu den Standard Zugriffsrechten unterstützt.



| Wert                             | Bedeutung                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Timer \_ Sämtlicher \_ Zugriff** (0x1F 0003) | Alle möglichen Zugriffsrechte für ein Aktivier bares Zeit Geber Objekt. Verwenden Sie dieses Recht nur, wenn die Anwendung über den Standard-Zugriffsrechte und den Zeit Geber Änderungs **\_ \_ Status** hinaus Zugriff erfordert. Die Verwendung dieses Zugriffsrechts erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **Timer \_ \_Zustand ändern** (0x0002) | Ändern des Zustands Zugriffs, der für die Funktionen " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) " und " [**cancelwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) " erforderlich ist.                                                                                                                                            |
| **Timer \_ Abfrage \_ Status** (0x0001)  | Für die zukünftige Verwendung reserviert.                                                                                                                                                                                                                                                                                 |



 

Um die SACL eines prozessübergreifenden Synchronisierungs Objekts zu lesen oder zu schreiben, müssen Sie das **Zugriffs \_ System- \_ Sicherheits** Zugriffsrecht anfordern. Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](../secauthz/access-control-lists.md) und [SACL-Zugriffsrecht](../secauthz/sacl-access-right.md).

 

 

---
description: Mit dem Windows Sicherheitsmodell können Sie den Zugriff auf Ereignis-, Mutex-, Semaphor- und wartebare Timerobjekte steuern. Timerwarteschlangen, interlockierte Variablen und kritische Abschnittsobjekte sind nicht sicherungsfähig. Weitere Informationen finden Sie unter Access-Control-Modell.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Sicherheit und Zugriffsrechte für Synchronisierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85ca76002a92e305983ab97d46dfde2f36f9ae49a779e091a072d3090ceb976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739290"
---
# <a name="synchronization-object-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für Synchronisierungsobjekte

Mit dem Windows Sicherheitsmodell können Sie den Zugriff auf Ereignis-, Mutex-, Semaphor- und wartebare Timerobjekte steuern. Timerwarteschlangen, interlockierte Variablen und kritische Abschnittsobjekte sind nicht sicherungsfähig. Weitere Informationen finden Sie unter [Access-Control Model](../secauthz/access-control-model.md).

Sie können eine [Sicherheitsbeschreibung](../secauthz/security-descriptors.md) für ein prozessübergreifendes Synchronisierungsobjekt angeben, wenn Sie die Funktion [**CreateEvent,**](/windows/win32/api/synchapi/nf-synchapi-createeventa) [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)oder [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) aufrufen. Wenn Sie **NULL** angeben, ruft das -Objekt einen Standardsicherheitsdeskriptor ab. Die [Zugriffssteuerungslisten (Access-Control Lists, ACLs)](../secauthz/access-control-lists.md) in der Standardsicherheitsbeschreibung für ein Synchronisierungsobjekt stammen aus dem primären Token oder Identitätswechseltoken des Erstellers.

Rufen Sie die Funktionen [**GetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)oder [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) auf, um die Sicherheitsbeschreibung eines Ereignis-, Mutex-, Semaphor- oder wartebaren Timerobjekts abzurufen oder festzulegen.

Die von [**CreateEvent,**](/windows/win32/api/synchapi/nf-synchapi-createeventa) [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)und [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) zurückgegebenen Handles haben Vollzugriff auf das neue Objekt. Wenn Sie die Funktionen [**OpenEvent,**](/windows/win32/api/synchapi/nf-synchapi-openeventa) [**OpenMutex,**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)und [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) aufrufen, überprüft das System die angeforderten Zugriffsrechte anhand des Sicherheitsdeskriptors des Objekts.

Die gültigen Zugriffsrechte für die prozessübergreifenden Synchronisierungsobjekte umfassen die [Standardzugriffsrechte](../secauthz/standard-access-rights.md) und einige objektspezifische Zugriffsrechte. In der folgenden Tabelle sind die Standardzugriffsrechte aufgeführt, die von allen -Objekten verwendet werden.

| Wert                           | Bedeutung                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DELETE** (0x00010000L)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                           |
| **LESEN \_ CONTROL** (0x00020000L) | Erforderlich, um Informationen in der Sicherheitsbeschreibung für das Objekt zu lesen, ohne die Informationen in der SACL einzulesen. Zum Lesen oder Schreiben der SACL müssen Sie das **Zugriffsrecht ACCESS \_ SYSTEM \_ SECURITY** anfordern. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht.](../secauthz/sacl-access-right.md) |
| **SYNCHRONIZE** (0x00100000L)   | Das Recht, das Objekt für die Synchronisierung zu verwenden. Dadurch kann ein Thread warten, bis sich das Objekt im signalisierten Zustand befindet.                                                                                                                                                                |
| **WRITE \_ DAC** (0x00040000L)    | Erforderlich, um die DACL in der Sicherheitsbeschreibung für das Objekt zu ändern.                                                                                                                                                                                                                   |
| **WRITE \_ OWNER** (0x00080000L)  | Erforderlich, um den Besitzer in der Sicherheitsbeschreibung für das Objekt zu ändern.                                                                                                                                                                                                                  |



 

In der folgenden Tabelle sind die objektspezifischen Zugriffsrechte für Ereignisobjekte aufgeführt. Diese Rechte werden zusätzlich zu den Standardzugriffsrechten unterstützt.



| Wert                             | Bedeutung                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ ALL \_ ACCESS** (0x1F0003) | Alle möglichen Zugriffsrechte für ein Ereignisobjekt. Verwenden Sie dieses Recht nur, wenn Ihre Anwendung Zugriff benötigt, der über den durch die Standardzugriffsrechte und **EVENT \_ MODIFY \_ STATE** gewährten Zugriff hinausgeht. Die Verwendung dieses Zugriffsrechtes erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **EVENT \_ MODIFY \_ STATE** (0x0002) | Ändern Sie den Zustandszugriff, der für die Funktionen [**SetEvent,**](/windows/win32/api/synchapi/nf-synchapi-setevent) [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) und [**PulseEvent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) erforderlich ist.                                                                                                                                    |



 

In der folgenden Tabelle sind die objektspezifischen Zugriffsrechte für Mutex-Objekte aufgeführt. Diese Rechte werden zusätzlich zu den Standardzugriffsrechten unterstützt.



| Wert                             | Bedeutung                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MUTEX \_ ALL \_ ACCESS** (0x1F0001) | Alle möglichen Zugriffsrechte für ein Mutexobjekt. Verwenden Sie dieses Recht nur, wenn Ihre Anwendung Zugriff benötigt, der über den durch die Standardzugriffsrechte gewährten Zugriff hinausgeht. Die Verwendung dieses Zugriffsrechtes erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **MUTEX \_ MODIFY \_ STATE** (0x0001) | Für die zukünftige Verwendung reserviert.                                                                                                                                                                                                                                           |



 

In der folgenden Tabelle sind die objektspezifischen Zugriffsrechte für Semaphorobjekte aufgeführt. Diese Rechte werden zusätzlich zu den Standardzugriffsrechten unterstützt.



| Wert                                 | Bedeutung                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEMAPHORE \_ ALL \_ ACCESS** (0x1F0003) | Alle möglichen Zugriffsrechte für ein Semaphorobjekt. Verwenden Sie dieses Recht nur, wenn Ihre Anwendung Zugriff benötigt, der über den durch die Standardzugriffsrechte und **SEMAPHORE \_ MODIFY \_ STATE** gewährten Zugriff hinausgeht. Die Verwendung dieses Zugriffsrechtes erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **SEMAPHORE \_ MODIFY \_ STATE** (0x0002) | Ändern Sie den Zustandszugriff, der für die [**ReleaseSemaphore-Funktion**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) erforderlich ist.                                                                                                                                                                                                   |



 

In der folgenden Tabelle sind die objektspezifischen Zugriffsrechte für wartende Timerobjekte aufgeführt. Diese Rechte werden zusätzlich zu den Standardzugriffsrechten unterstützt.



| Wert                             | Bedeutung                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TIMER \_ ALL \_ ACCESS** (0x1F0003) | Alle möglichen Zugriffsrechte für ein wartebares Timerobjekt. Verwenden Sie dieses Recht nur, wenn Ihre Anwendung Zugriff benötigt, der über den durch die Standardzugriffsrechte und **TIMER \_ MODIFY \_ STATE** gewährten Zugriff hinausgeht. Die Verwendung dieses Zugriffsrechtes erhöht die Wahrscheinlichkeit, dass Ihre Anwendung von einem Administrator ausgeführt werden muss. |
| **TIMER \_ MODIFY \_ STATE** (0x0002) | Ändern Sie den Zustandszugriff, der für die Funktionen [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) und [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) erforderlich ist.                                                                                                                                            |
| **TIMER \_ QUERY \_ STATE** (0x0001)  | Für die zukünftige Verwendung reserviert.                                                                                                                                                                                                                                                                                 |



 

Um die SACL eines prozessübergreifenden Synchronisierungsobjekts zu lesen oder zu schreiben, müssen Sie das **Zugriffsrecht ACCESS \_ SYSTEM \_ SECURITY** anfordern. Weitere Informationen finden Sie unter [Zugriffssteuerungslisten (ACLs)](../secauthz/access-control-lists.md) und [SACL-Zugriffsrecht.](../secauthz/sacl-access-right.md)

 

 

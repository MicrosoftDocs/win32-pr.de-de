---
description: Das Microsoft Windows-Sicherheitsmodell ermöglicht es Ihnen, den Zugriff auf Auftrags Objekte zu steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control Modell.
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: Sicherheit und Zugriffsrechte für das Auftrags Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5207e459bab2ae444282355844401e0b82e9c
ms.sourcegitcommit: 18023a15a4312c653a8dcc0feef23e3413a7f5dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "106354243"
---
# <a name="job-object-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für das Auftrags Objekt

Das Microsoft Windows-Sicherheitsmodell ermöglicht es Ihnen, den Zugriff auf Auftrags Objekte zu steuern. Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](../secauthz/access-control-model.md).

Sie können eine [Sicherheits Beschreibung](../secauthz/security-descriptors.md) für ein Auftrags Objekt angeben, wenn Sie die Funktion "up- [**JobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) " aufrufen. Wenn Sie NULL angeben, erhält das Auftrags Objekt eine Standard Sicherheits Beschreibung. Die ACLs in der Standard Sicherheits Beschreibung für ein Auftrags Objekt stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.

Um die Sicherheits Beschreibung für ein Auftrags Objekt abzurufen oder festzulegen, müssen Sie die Funktion [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)oder [**setsecurityinfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) aufrufen.

Zu den gültigen Zugriffsrechten für Auftrags Objekte gehören die [Standard Zugriffsrechte](../secauthz/standard-access-rights.md) und einige auftragsspezifische Zugriffsrechte. In der folgenden Tabelle sind die standardmäßigen Zugriffsrechte aufgelistet, die von allen Objekten verwendet werden.

| Wert                           | Bedeutung                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Delete** (0x00010000l)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                           |
| **Lesen Sie \_ Control** (0x00020000l) | Ist erforderlich, um Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen. Um die SACL zu lesen oder zu schreiben, müssen Sie das **Zugriffs \_ System- \_ Sicherheits** Zugriffsrecht anfordern. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](../secauthz/sacl-access-right.md). |
| **Synchronisieren** (0x00100000l)   | Das Recht, das Objekt für die Synchronisierung zu verwenden. Dadurch kann ein Thread warten, bis sich das Objekt im signalisierten Zustand befindet.                                                                                                                                                                |
| **Schreiben \_ DAC** (0x00040000l)    | Erforderlich, um die DACL in der Sicherheits Beschreibung für das-Objekt zu ändern.                                                                                                                                                                                                                   |
| **Schreiben \_ Besitzer** (0x00080000l)  | Erforderlich, um den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.                                                                                                                                                                                                                  |



 

In der folgenden Tabelle sind die auftragsspezifischen Zugriffsrechte aufgeführt.



| Wert                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Auftrag \_ Object \_ All \_ Access** (0x1F 001F)             | Kombiniert alle gültigen Zugriffsrechte für das Auftrags Objekt.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Auftrag \_ Objekt \_ Zuweisungs \_ Prozess** (0x0001)           | Ist erforderlich, um die Funktion "Assign [**processtojobobject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) " zum Zuweisen von Prozessen zum Auftrags Objekt aufzurufen.                                                                                                                                                                                                                                                                                                                                                                |
| **Auftrag \_ Objekt \_ Abfrage** (0x0004)                     | Erforderlich zum Abrufen bestimmter Informationen über ein Auftrags Objekt, z. b. Attribute und Buchhaltungsinformationen (siehe [**queryinformationjobobject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) und [**isprocessinjob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)).                                                                                                                                                                                                                                                                    |
| **Auftrag \_ \_Objektset- \_ Attribute** (0x0002)           | Zum Aufrufen der [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) -Funktion erforderlich, um die Attribute des Auftrags Objekts festzulegen.                                                                                                                                                                                                                                                                                                                                                                |
| **Auftrag \_ \_Objektset- \_ Sicherheits \_ Attribute** (0x0010) | Dieses Flag wird nicht unterstützt. Sicherheitseinschränkungen müssen für jeden Prozess, der einem Auftrags Objekt zugeordnet ist, einzeln festgelegt werden. **Windows Server 2003 und Windows XP:** Ist erforderlich, um die [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) -Funktion mit der **jobobjectsecuritylimitinformation** -Informations Klasse aufzurufen, um Sicherheitseinschränkungen für die Prozesse festzulegen, die dem Auftrags Objekt zugeordnet sind. Die Unterstützung für dieses Flag wurde in Windows Vista und Windows Server 2008 entfernt. <br/> |
| **Auftrag \_ Objekt \_ Beenden** (0x0008)                 | Ist erforderlich, um die [**terminatejobobject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) -Funktion zum Beenden aller Prozesse im Auftrags Objekt aufzurufen.                                                                                                                                                                                                                                                                                                                                                                     |



 

Das von " [**kreatejobobject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) " zurückgegebene Handle verfügt über ein **Auftrags \_ Objekt \_ \_** , das Zugriff auf das Auftrags Objekt hat. Wenn Sie die [**openjobobject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) -Funktion aufrufen, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Objekts. Wenn sich ein Auftrags Objekt in einer Hierarchie von [gedugten Aufträgen](nested-jobs.md)befindet, kann ein Aufrufer mit Zugriff auf das Auftrags Objekt implizit auf alle seine untergeordneten Aufträge in der Hierarchie zugreifen.

Sie können das Zugriffs **\_ System- \_ Sicherheits** Zugriffsrecht für ein Auftrags Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](../secauthz/access-control-lists.md) und [SACL-Zugriffsrecht](../secauthz/sacl-access-right.md).

Sicherheitseinschränkungen müssen für jeden Prozess, der einem Auftrags Objekt zugeordnet ist, einzeln festgelegt werden, anstatt Sie für das Auftrags Objekt selbst festzulegen. Weitere Informationen finden Sie unter [Prozesssicherheit und Zugriffsrechte](process-security-and-access-rights.md).

**Windows Server 2003 und Windows XP:** Sie können die Funktion [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) verwenden, um Sicherheitseinschränkungen für das Auftrags Objekt festzulegen. Diese Funktion wurde in Windows Vista und Windows Server 2008 entfernt.

 

 

---
title: Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte
description: Wenn Sie in Active Directory Domain Services ein neues Objekt erstellen, können Sie explizit eine Sicherheits Beschreibung erstellen und diese Sicherheits Beschreibung dann als ntSecurityDescriptor-Eigenschaft des Objekts festlegen.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- Objekte AD, wie Sicherheits Deskriptoren für neue Verzeichnisobjekte festgelegt werden
- Sicherheits Beschreibungen AD, Vorgehensweise beim Festlegen von auf neuen Verzeichnis Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7858d08944e93165b4a1a63ef7d845ee646dc648
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472540"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte

Wenn Sie in Active Directory Domain Services ein neues Objekt erstellen, können Sie explizit eine Sicherheits Beschreibung erstellen und diese Sicherheits Beschreibung dann als **ntSecurityDescriptor** -Eigenschaft des Objekts festlegen. Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Verzeichnis Objekt](creating-a-security-descriptor-for-a-new-directory-object.md).

Active Directory Domain Services verwenden Sie die folgenden Regeln, um die DACL in der Sicherheits Beschreibung des neuen Objekts festzulegen:

-   Wenn Sie beim Erstellen des Objekts explizit eine Sicherheits Beschreibung angeben, führt das System alle vererbbaren ACEs aus dem übergeordneten Objekt in der angegebenen DACL zusammen, es sei denn, das **\_ \_ geschützte SE-DACL** -Bit wird in den Steuerungs Bits der Sicherheits Beschreibung festgelegt.
-   Wenn Sie keine Sicherheits Beschreibung angeben, erstellt das System die DACL des Objekts, indem alle vererbbaren ACEs aus dem übergeordneten Objekt aus dem **classSchema** -Objekt für die Klasse des Objekts zusammengeführt werden.
-   Wenn das Schema nicht über eine standardmäßige DACL verfügt, ist die DACL des Objekts die Standard-DACL vom primären oder Identitätswechsel Token des Erstellers.
-   Wenn keine angegebene, geerbte oder standardmäßige DACL vorhanden ist, erstellt das System das Objekt ohne DACL, das allen vollständigen Zugriff auf das Objekt ermöglicht.

Das System verwendet einen ähnlichen Algorithmus, um eine SACL für ein Verzeichnisdienst Objekt zu erstellen.

Der Besitzer und die primäre Gruppe in der Sicherheits Beschreibung des neuen Objekts werden auf die Werte festgelegt, die Sie in der Eigenschaft **ntSecurityDescriptor** angeben, wenn Sie das Objekt erstellen. Wenn Sie diese Werte nicht festlegen, Active Directory Domain Services die in der folgenden Tabelle aufgeführten Regeln verwenden, um Sie festzulegen.



| Regel          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Besitzer         | Der Besitzer in einer Standard Sicherheits Beschreibung wird auf die standardmäßige Besitzer-SID aus dem primären Token oder dem Identitätswechsel Token des erstellenden Prozesses festgelegt. Für die meisten Benutzer ist die standardmäßige Besitzer-SID identisch mit der SID, die das Konto des Benutzers identifiziert. Beachten Sie, dass das System für Benutzer, die Mitglieder der integrierten Gruppe "Administratoren" sind, automatisch die Standard Besitzer-SID im Zugriffs Token für die Gruppe "Administratoren" festlegt. Daher sind Objekte, die von einem Mitglied der Gruppe "Administratoren" erstellt werden, in der Regel der Gruppe "Administratoren" angehören. Um den Standard Besitzer in einem Zugriffs Token abzurufen oder festzulegen, müssen Sie die [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -oder [**settokeninformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) -Funktion mit der tokenbesitzerstruktur aufrufen. [**\_**](/windows/desktop/api/winnt/ns-winnt-token_owner) |
| Primäre Gruppe | Die primäre Gruppe in einer Standard Sicherheits Beschreibung wird auf die primäre Standardgruppe aus dem primären oder Identitäts Token des Erstellers festgelegt. Beachten Sie, dass die primäre Gruppe nicht im Kontext von Active Directory Domain Services verwendet wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Weitere Informationen zur ACE-Vererbung finden Sie unter [Vererbung und Delegierung der Verwaltung](inheritance-and-delegation-of-administration.md).

Weitere Informationen zu den Standard Sicherheits Deskriptoren im Schema finden Sie unter [Standard Sicherheits Beschreibung](default-security-descriptor.md).

Weitere Informationen zu **classSchema** -Objekten finden Sie unter [Active Directory Schema](active-directory-schema.md).

 

 
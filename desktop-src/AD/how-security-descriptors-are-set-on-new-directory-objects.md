---
title: Festlegen von Sicherheitsdeskriptoren für neue Verzeichnisobjekte
description: Wenn Sie ein neues -Objekt in Active Directory Domain Services erstellen, können Sie explizit einen Sicherheitsdeskriptor erstellen und diesen Sicherheitsdeskriptor dann als nTSecurityDescriptor-Eigenschaft des Objekts festlegen.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- Objekte AD , wie Sicherheitsdeskriptoren für neue Verzeichnisobjekte festgelegt werden
- Sicherheitsdeskriptoren AD , festlegen für neue Verzeichnisobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d2009367c4d5604d359913b0154320332cd4be58e50dc5f065c574f8ea5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188111"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Festlegen von Sicherheitsdeskriptoren für neue Verzeichnisobjekte

Wenn Sie ein neues -Objekt in Active Directory Domain Services erstellen, können Sie explizit einen Sicherheitsdeskriptor erstellen und diesen Sicherheitsdeskriptor dann als **nTSecurityDescriptor-Eigenschaft** des Objekts festlegen. Weitere Informationen finden Sie unter [Erstellen eines Sicherheitsdeskriptors für ein neues Verzeichnisobjekt.](creating-a-security-descriptor-for-a-new-directory-object.md)

Active Directory Domain Services verwenden Sie die folgenden Regeln, um die DACL im Sicherheitsdeskriptor des neuen Objekts fest zu legen:

-   Wenn Sie beim Erstellen des Objekts explizit einen Sicherheitsdeskriptor angeben, führt das System alle vererbten ACEs aus dem übergeordneten Objekt mit der angegebenen DACL zusammen, es sei denn, das **SE \_ DACL \_ PROTECTED-Bit** ist in den Steuerungsbits des Sicherheitsdeskriptors festgelegt.
-   Wenn Sie keinen Sicherheitsdeskriptor angeben, erstellt das System die DACL des Objekts, indem alle vererbten ACEs aus dem übergeordneten Objekt mit der Standard-DACL aus dem **classSchema-Objekt** für die -Klasse des Objekts zusammengeführt werden.
-   Wenn das Schema nicht über eine Standard-DACL verfügt, ist die DACL des Objekts die Standard-DACL aus dem primären Token oder Identitätswechseltoken des Erstellers.
-   Wenn keine angegebene, geerbte oder Standard-DACL angegeben ist, erstellt das System das Objekt ohne DACL, wodurch jeder Vollzugriff auf das Objekt ermöglicht wird.

Das System verwendet einen ähnlichen Algorithmus, um eine SACL für ein Verzeichnisdienstobjekt zu erstellen.

Der Besitzer und die primäre Gruppe im Sicherheitsdeskriptor des neuen Objekts werden auf die Werte festgelegt, die Sie beim Erstellen des Objekts in der **nTSecurityDescriptor-Eigenschaft** angeben. Wenn Sie diese Werte nicht festlegen, Active Directory Domain Services sie mithilfe der in der folgenden Tabelle aufgeführten Regeln festlegen.



| Regel          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Besitzer         | Der Besitzer in einer Standardsicherheitsbeschreibung wird auf die Standardbesitzer-SID aus dem primären Token oder Identitätswechseltoken des Erstellungsprozesses festgelegt. Für die meisten Benutzer ist die Standardbesitzer-SID mit der SID identisch, die das Benutzerkonto identifiziert. Beachten Sie, dass das System für Benutzer, die Mitglieder der integrierten Administratorgruppe sind, automatisch die Standardbesitzer-SID im Zugriffstoken auf die Administratorengruppe fest. Daher befinden sich Objekte, die von einem Mitglied der Administratorengruppe erstellt wurden, in der Regel im Besitz der Administratorengruppe. Rufen Sie zum Abrufen oder Festlegen des Standardbesitzers in einem Zugriffstoken die [**Funktion GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) oder [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) mit der [**TOKEN \_ OWNER-Struktur**](/windows/desktop/api/winnt/ns-winnt-token_owner) auf. |
| Primäre Gruppe | Die primäre Gruppe in einer Standardsicherheitsbeschreibung wird auf die primäre Standardgruppe aus dem primären Token oder Identitätswechseltoken des Erstellers festgelegt. Beachten Sie, dass die primäre Gruppe nicht im Kontext der Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Weitere Informationen zur ACE-Vererbung finden Sie unter [Vererbung und Delegierung der Verwaltung.](inheritance-and-delegation-of-administration.md)

Weitere Informationen zu den Standardsicherheitsdeskriptoren im Schema finden Sie unter [Standardsicherheitsdeskriptor](default-security-descriptor.md).

Weitere Informationen zu **classSchema-Objekten** finden Sie unter [Active Directory-Schema](active-directory-schema.md).

 

 
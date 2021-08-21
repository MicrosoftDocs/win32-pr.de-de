---
title: Access Control und Objekterstellung
description: Der Active Directory-Server kann kein untergeordnetes Objekt erstellen, wenn der Aufrufer nicht über ads \_ right \_ ds \_ create child für \_ diesen Objekttyp im übergeordneten Container verfügt.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Access Control und Objekterstellungs-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b99251cd9c9c93177e0b6cfc362c7003078c870e809b48c9aba351e620e1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025723"
---
# <a name="access-control-and-object-creation"></a>Access Control und Objekterstellung

Der Active Directory-Server kann kein untergeordnetes Objekt erstellen, wenn der Aufrufer nicht über ads **\_ right \_ ds create \_ \_ child** für diesen Objekttyp im übergeordneten Container verfügt. Um die Typen von untergeordneten Objekten zu bestimmen, die der Aufrufer in einem Verzeichnisobjekt erstellen kann, lesen Sie das **allowedChildClassesEffective-Attribut** des Objekts.

Wenn Sie die [**IADsContainer::Create-Methode**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) verwenden, um ein untergeordnetes Objekt zu erstellen, wird das Objekt erst persistent, [**wenn IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) für das neue Objekt aufgerufen wird. Zwischen den **Aufrufen Create** und **SetInfo** kann der erstellende Thread Werte in die Eigenschaften des neuen Objekts setzen. Nach dem **SetInfo-Aufruf** verfügt der erstellende Thread nicht unbedingt über die Zugriffsrechte zum Festlegen der Eigenschaften des neuen Objekts. Um sicherzustellen, dass der Aufrufer über diese Rechte verfügt, geben Sie während der Erstellung einen expliziten Sicherheitsdeskriptor an. Die DACL sollte über einen ACE verfügen, der dem Aufrufer die erforderlichen Zugriffsrechte für das Objekt erteilt.

Weitere Informationen zur Zugriffssteuerung und Objekterstellung finden Sie unter Festlegen von [Sicherheitsbeschreibungen für neue Verzeichnisobjekte.](how-security-descriptors-are-set-on-new-directory-objects.md)

 

 
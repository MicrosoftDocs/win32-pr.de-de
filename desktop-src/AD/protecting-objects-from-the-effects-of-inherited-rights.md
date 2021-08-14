---
title: Schützen von Objekten vor den Auswirkungen geerbter Rechte
description: Wie im Thema Vererbung und Delegierung der Verwaltung erläutert, können ACEs für ein Containerobjekt wie organizationalUnit, domainDNS, container und so weiter festgelegt und auf Grundlage der für diese ACEs festgelegten ACE-Flags an untergeordnete Objekte propagiert werden.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Schützen von Objekten vor den Auswirkungen von geerbten Rechte-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcc1067fcfe0d57e2e7aca837b97d73f18b55a41a4f1347ac36224b987918aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185015"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Schützen von Objekten vor den Auswirkungen geerbter Rechte

Wie im Thema Vererbung und Delegierung der Verwaltung [erläutert,](inheritance-and-delegation-of-administration.md)können ACEs für ein Containerobjekt festgelegt werden, z. B. **eine organizationalUnit,** **domainDNS,** **container** und so weiter, und auf der Grundlage der für diese ACEs festgelegten ACE-Flags an untergeordnete Objekte propagiert werden.

Wenn Sie über ein sicheres Objekt oder ein Objekt verfügen, dessen ACEs Sie explizit steuern möchten, z. B. eine private Organisationseinheit oder ein spezieller Benutzer, können Sie verhindern, dass ACEs durch den übergeordneten Container oder die Vorgänger des übergeordneten Containers an das Objekt propagiert werden.

Verwenden Sie die [**IADsSecurityDescriptor.Control-Eigenschaft,**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) um zu steuern, ob DACLs und SACLs vom Objekt aus dem übergeordneten Container geerbt werden.

Die [**IADsSecurityDescriptor.Control-Eigenschaft**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) kann verwendet werden, um ein Objekt vor den Auswirkungen geerbter ACEs zu schützen. Die folgenden Flags erzwingen, dass die Zugriffssteuerung explizit für das Objekt festgelegt wird, und verhindern, dass ein Benutzer die Zugriffssteuerung auf das Objekt ändert, indem er vererbbare ACEs für den übergeordneten Container des Objekts oder die Vorgänger des übergeordneten Containers festlegen.



| Flag                               | Beschreibung                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_SE DACL \_ PROTECTED**<br/> | Verhindert, dass ACEs, die für die DACL des übergeordneten Containers festgelegt sind, und alle Objekte über dem übergeordneten Container in der Verzeichnishierarchie auf die Objekt-DACL angewendet werden.<br/> |
| **\_SE SACL \_ PROTECTED**<br/> | Verhindert, dass ACEs, die für die SACL des übergeordneten Containers festgelegt sind, und alle Objekte über dem übergeordneten Container in der Verzeichnishierarchie auf das Objekt SACL angewendet werden.<br/> |



 

Beachten Sie, dass das **SE \_ DACL \_ PRESENT-Flag** vorhanden sein muss, um SE **\_ DACL \_ PROTECTED** und **SE \_ SACL \_ PRESENT** zum Festlegen von **\_ SACL PROTECTED \_ SE.**

 


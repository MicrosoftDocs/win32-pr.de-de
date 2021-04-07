---
title: Schützen von Objekten vor den Auswirkungen von geerbten rechten
description: Wie im Thema Vererbung und Delegierung der Verwaltung erläutert, kann ACEs für ein Container Objekt festgelegt werden, z. b. eine OrganizationalUnit, eine domainDNS, einen Container usw., und basierend auf den ACE-Flags, die für diese ACEs festgelegt wurden, an untergeordnete Objekte weitergegeben.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Schützen von Objekten vor den Auswirkungen von geerbten rechten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038743"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Schützen von Objekten vor den Auswirkungen von geerbten rechten

Wie im Thema [Vererbung und Delegierung der Verwaltung](inheritance-and-delegation-of-administration.md)erläutert, kann ACEs für ein Container Objekt festgelegt werden, z. b. eine **OrganizationalUnit**, eine **domainDns**, einen **Container** usw., und basierend auf den ACE-Flags, die für diese ACEs festgelegt wurden, an untergeordnete Objekte weitergegeben.

Wenn Sie über ein sicheres Objekt oder ein Objekt verfügen, dessen ACEs Sie explizit steuern möchten (z. b. eine private OE oder ein spezieller Benutzer), können Sie verhindern, dass ACEs über den übergeordneten Container oder die Vorgänger des übergeordneten Containers an das Objekt weitergegeben werden.

Verwenden Sie die Eigenschaft [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) , um zu steuern, ob DACLs und SACLs von dem Objekt von seinem übergeordneten Container geerbt werden.

Die [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Eigenschaft kann verwendet werden, um ein Objekt vor den Auswirkungen von geerbten ACEs zu schützen. Die folgenden Flags erzwingen, dass die Zugriffs Steuerung explizit für das-Objekt festgelegt wird, und verhindern, dass ein Benutzer die Zugriffs Steuerung für das Objekt ändert, indem vererbbare ACEs für den übergeordneten Container des Objekts oder die Vorgänger des übergeordneten Containers festgelegt werden.



| Flag                               | Beschreibung                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SE \_ DACL \_ Protected**<br/> | Verhindert, dass für die DACL des übergeordneten Containers festgelegte ACEs und alle Objekte oberhalb des übergeordneten Containers in der Verzeichnishierarchie auf die DACL des Objekts angewendet werden.<br/> |
| **SE \_ SACL \_ Protected**<br/> | Verhindert, dass für die SACL des übergeordneten Containers festgelegte ACEs und alle Objekte oberhalb des übergeordneten Containers in der Verzeichnishierarchie auf die SACL des Objekts angewendet werden.<br/> |



 

Beachten Sie, dass das Flag für die **SE \_ DACL- \_ Darstellung** vorhanden sein muss, um die **SE \_ DACL- \_ geschützte** und **SE- \_ SACL \_** vorhanden zu **legen \_ \_**

 


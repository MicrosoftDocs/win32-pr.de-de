---
title: Bindungsprobleme für gemischte Umgebungen
description: Bindungsprobleme für gemischte Umgebungen
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindungsprobleme für gemischte Umgebungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337677"
---
# <a name="binding-issues-for-mixed-environments"></a>Bindungsprobleme für gemischte Umgebungen

Für Umgebungen, in denen die Domäne, die Active Directory enthält, eine Vertrauensstellung mit einer Windows NT 4,0-Domäne hat, kann ein Problem mit der Verwendung der Server losen Bindung zum Binden an Active Directory Objekte auftreten.

In einigen Netzwerkumgebungen wurden Vertrauens Stellungen zwischen Domänen Controllern eingerichtet, die Active Directory-und Windows NT 4,0-Server enthalten, um die Authentifizierung zwischen Domänen zuzulassen. Wenn ein Benutzer, der Mitglied von Windows NT 4,0 ist, in diesen gemischten Umgebungen versucht, eine Server lose Bindung zu verwenden, um eine Bindung an ein Active Directory Objekt in einer vertrauenswürdigen Domäne herzustellen, schlägt die Bindung fehl, und es wird ein Fehler zurückgegeben. Dies liegt daran, dass eine Server lose Bindung die [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) -Funktion verwendet, um eine Bindung an das Objekt in Active Directory herzustellen, das von dem richtigen DNS abhängig ist.

In diesem Szenario muss der Windows NT-Benutzer den Namen einer bestimmten Domäne angeben, an die eine Bindung erfolgen soll. Im Folgenden finden Sie ein Beispiel.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 
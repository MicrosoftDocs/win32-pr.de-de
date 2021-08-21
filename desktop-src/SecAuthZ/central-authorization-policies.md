---
description: Eine zentrale Autorisierungsrichtlinie (Central Authorization Policy, CAP) erfasst die spezifischen Autorisierungsregeln (CAPRs) in einer einzigen Richtlinie.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Zentrale Autorisierungsrichtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0617f6bddb606d3c3fb3e5ccb6692c79c62a60f90de591b6ec3e04988db46f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783224"
---
# <a name="central-authorization-policies"></a>Zentrale Autorisierungsrichtlinien

Eine zentrale Autorisierungsrichtlinie (Central Authorization Policy, CAP) erfasst die spezifischen Autorisierungsregeln (CAPRs) in einer einzigen Richtlinie. Damit die spezifischen Autorisierungsregeln (CAPRs) in der ganzheitlichen Autorisierungsrichtlinie der Organisation kombiniert werden können, können caprs zusammen referenziert und auf eine Gruppe von Ressourcen angewendet werden. Dies erfolgt, indem mehrere (als Verweis) in einer CAP gesammelt werden. Sobald eine CAP definiert ist, kann sie von Ressourcen-Managern genutzt werden, um die Autorisierungsrichtlinie der Organisation auf Ressourcen anzuwenden.

Eine CAP weist die folgenden Attribute auf:

-   Sammlung von CAPRs : eine Liste von Verweisen auf vorhandene CAPR-Objekte
-   Ein Bezeichner (Sid)
-   Beschreibung
-   Name

Eine CAP wird während der Zugriffsauswertung für Dateien und Ordner ausgewertet, für die ein Administrator sie aktiviert. Während eines [**AccessCheck-Aufrufs**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) wird die CAP-Überprüfung logisch mit der diskreten ACL-Überprüfung kombiniert. Dies bedeutet, dass ein Benutzer Zugriff sowohl gemäß der CAP (den zugehörigen CAPRs) als auch gemäß der frei zugänglichen ACL für die Datei haben muss, um Zugriff auf eine Datei zu erhalten, für die die CAP gilt.

Cap-Beispiel:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>CAP-Definition

Eine CAP wird in Active Directory mithilfe einer neuen Benutzererfahrung in ADAC (oder PowerShell) erstellt und bearbeitet, die es dem Administrator ermöglicht, eine CAP zu erstellen und einen Satz von CAPRs anzugeben, aus denen die CAP besteht.

 

 

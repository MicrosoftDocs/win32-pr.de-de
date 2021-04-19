---
description: Eine zentrale Autorisierungs Richtlinie (Cap) sammelt die spezifischen Autorisierungs Regeln (caprs) in einer einzelnen Richtlinie.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Zentrale Autorisierungs Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347025"
---
# <a name="central-authorization-policies"></a>Zentrale Autorisierungs Richtlinien

Eine zentrale Autorisierungs Richtlinie (Cap) sammelt die spezifischen Autorisierungs Regeln (caprs) in einer einzelnen Richtlinie. Damit die spezifischen Autorisierungs Regeln (caprs) in der ganzheitlichen Autorisierungs Richtlinie der Organisation zusammengefasst werden können, kann auf caprs zusammen verwiesen und auf einen Satz von Ressourcen angewendet werden. Dies erfolgt durch das Erfassen mehrerer (als Verweis) in eine Obergrenze. Sobald eine Obergrenze definiert ist, kann Sie von Ressourcen-Managern genutzt werden, um die Autorisierungs Richtlinie für Organisationen auf Ressourcen anzuwenden.

Eine Obergrenze hat die folgenden Attribute:

-   Sammlung von caprs – eine Liste mit Verweisen auf vorhandene Capr-Objekte
-   Ein Bezeichner (SID)
-   BESCHREIBUNG
-   Name

Eine Obergrenze wird während der Zugriffs Auswertung für Dateien und Ordner ausgewertet, in denen Sie von einem Administrator aktiviert wird. Während eines [**Access Check**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Aufrufes wird die Cap-Prüfung logisch mit der Überprüfung der freigegebenen Zugriffs Steuerungs Liste kombiniert. Dies bedeutet, dass ein Benutzer für den Zugriff auf eine Datei, auf die das Cap angewendet wird, über Zugriff verfügen muss, und zwar gemäß der Obergrenze (zugeordneten caprs) und der freigegebenen ACL für die Datei.

Beispiel Obergrenze:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Cap-Definition

Eine Obergrenze wird in Active Directory mithilfe einer neuen Benutzeroberfläche in ADAC (oder PowerShell) erstellt und bearbeitet, die es dem Administrator ermöglicht, eine Obergrenze zu erstellen und einen Satz von caprs anzugeben, die die Obergrenze bilden.

 

 

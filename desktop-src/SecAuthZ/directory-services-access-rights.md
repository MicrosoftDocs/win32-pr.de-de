---
description: Jedem Active Directory-Objekt ist ein Sicherheitsdeskriptor zugewiesen.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Zugriffsrechte für Verzeichnisdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901c8eba5736750e0c91eb713993876c47858407110ca3c8ebc6ed8122e1b8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913763"
---
# <a name="directory-services-access-rights"></a>Zugriffsrechte für Verzeichnisdienste

Jedem Active Directory-Objekt ist ein [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) zugewiesen. In diesen Sicherheitsbeschreibungen kann ein Satz von Vertrauensnehmerrechten festgelegt werden, die für Verzeichnisdienstobjekte spezifisch sind. Diese Rechte sind in der folgenden Tabelle aufgeführt. Weitere Informationen finden Sie unter [Steuern von Zugriffsrechten.](/windows/desktop/AD/control-access-rights)



| Rechte                                | Bedeutung                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ OPEN<br/>            | Öffnen Sie ein DS-Objekt.<br/>                                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ CREATE \_ CHILD<br/>   | Erstellen Sie ein untergeordnetes DS-Objekt.<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ DELETE \_ CHILD<br/>   | Löscht ein untergeordnetes DS-Objekt.<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ LIST<br/>            | Aufzählen eines DS-Objekts.<br/>                                                                                                                                                                                                                                                       |
| ACTRL \_ DS \_ READ \_ PROP<br/>      | Lesen der Eigenschaften eines DS-Objekts.<br/>                                                                                                                                                                                                                                          |
| ACTRL \_ DS \_ WRITE \_ PROP<br/>     | Schreiben von Eigenschaften für ein DS-Objekt.<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ SELF<br/>            | Der Zugriff ist nur zulässig, nachdem überprüfte Rechteüberprüfungen durchgeführt wurden, die vom -Objekt unterstützt werden. Dieses Flag kann allein verwendet werden, um alle überprüften Rechteüberprüfungen des Objekts durchzuführen, oder es kann mit einem Bezeichner eines bestimmten überprüften Rechts kombiniert werden, um nur diese Überprüfung durchzuführen.<br/> |
| ACTRL \_ DS \_ DELETE \_ TREE<br/>    | Löscht eine Struktur von DS-Objekten.<br/>                                                                                                                                                                                                                                                 |
| ACTRL \_ DS \_ \_ LIST-OBJEKT<br/>    | Auflisten einer Struktur von DS-Objekten.<br/>                                                                                                                                                                                                                                                   |
| ACTRL \_ DS \_ CONTROL \_ ACCESS<br/> | Der Zugriff ist nur zulässig, nachdem erweiterte Rechteüberprüfungen durchgeführt wurden, die vom -Objekt unterstützt werden. Dieses Flag kann allein verwendet werden, um alle Überprüfungen erweiterter Rechte für das Objekt auszuführen, oder es kann mit einem Bezeichner eines bestimmten erweiterten Rechts kombiniert werden, um nur diese Überprüfung durchzuführen.<br/>    |



 

 


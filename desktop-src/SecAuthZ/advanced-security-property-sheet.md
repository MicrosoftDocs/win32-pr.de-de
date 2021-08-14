---
description: Mit dem Eigenschaftenblatt "Erweiterte Sicherheit" kann der Benutzer Bearbeitungsvorgänge ausführen, die auf der Eigenschaftenseite "Grundlegende Sicherheit" eines Zugriffssteuerungs-Editors nicht verfügbar sind.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Eigenschaftenblatt "Erweiterte Sicherheit"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808eaefaa481e828504eb55b3ecc3b70d487c03af82b296c3b8bc02da2b354d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914346"
---
# <a name="advanced-security-property-sheet"></a>Eigenschaftenblatt "Erweiterte Sicherheit"

Mit dem Eigenschaftenblatt "Erweiterte Sicherheit" kann der Benutzer Bearbeitungsvorgänge ausführen, die auf der [Eigenschaftenseite "Grundlegende Sicherheit"](basic-security-property-page.md) eines Zugriffssteuerungs-Editors nicht verfügbar sind. Das Eigenschaftenblatt kann die folgenden Eigenschaftenseiten enthalten:

-   Eine [Eigenschaftenseite Berechtigungen](permissions-property-page.md) für die erweiterte Bearbeitung der [*dacl (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des Objekts, z. B. bearbeiten [objektspezifische ACEs](object-specific-aces.md) oder Steuern der [ACE-Vererbung.](ace-inheritance.md)
-   Eine [Eigenschaftenseite "Überwachung"](auditing-property-page.md) zum Anzeigen und Bearbeiten der [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts.
-   Eine [Eigenschaftenseite "Besitzer"](owner-property-page.md) zum Ändern des Besitzers des Objekts.

Der Benutzer kann das Eigenschaftenblatt für die erweiterte Sicherheit anzeigen, indem er auf der Eigenschaftenseite "Grundlegende Sicherheit" auf die Schaltfläche **Erweitert** klickt. Um die Schaltfläche **Erweitert** anzuzeigen, legen Sie das SI \_ ADVANCED-Flag in der [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) fest, die von Ihrer [**ISecurityInformation::GetObjectInformation-Implementierung**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) zurückgegeben wird.

 

 

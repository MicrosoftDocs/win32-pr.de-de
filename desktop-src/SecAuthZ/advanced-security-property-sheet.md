---
description: Mithilfe des Eigenschaften Blatts erweiterte Sicherheit kann der Benutzer Bearbeitungsvorgänge ausführen, die auf der Eigenschaften Seite grundlegende Sicherheit eines Zugriffs Steuerungs-Editors nicht verfügbar sind.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Eigenschaften Blatt "Erweiterte Sicherheit"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369098"
---
# <a name="advanced-security-property-sheet"></a>Eigenschaften Blatt "Erweiterte Sicherheit"

Mithilfe des Eigenschaften Blatts erweiterte Sicherheit kann der Benutzer Bearbeitungsvorgänge ausführen, die auf der [Eigenschaften Seite grundlegende Sicherheit](basic-security-property-page.md) eines Zugriffs Steuerungs-Editors nicht verfügbar sind. Das Eigenschaften Blatt kann die folgenden Eigenschaften Seiten enthalten:

-   Eine [Berechtigungs](permissions-property-page.md) Eigenschaften Seite für die erweiterte Bearbeitung der [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts, z. b. das Bearbeiten [Objekt spezifischer ACEs](object-specific-aces.md) oder das Steuern der [ACE-Vererbung](ace-inheritance.md).
-   Eine [Eigenschaften](auditing-property-page.md) Seite für die Überwachung zum Anzeigen und Bearbeiten der [*System-Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts.
-   Eine Eigenschaften Seite des [Besitzers](owner-property-page.md) zum Ändern des Besitzers des Objekts.

Der Benutzer kann das Eigenschaften Blatt "Erweiterte Sicherheit" anzeigen, indem Sie auf der Eigenschaften Seite grundlegende Sicherheit auf die Schaltfläche **erweitert** klicken. Um die Schaltfläche **erweitert** anzuzeigen, legen Sie das Flag "Si \_ Advanced" in der Si-Objekt Informationsstruktur fest, die von Ihrer [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) -Implementierung zurückgegeben wurde. [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

 

 

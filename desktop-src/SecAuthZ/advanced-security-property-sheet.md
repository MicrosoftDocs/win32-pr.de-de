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
# <a name="advanced-security-property-sheet"></a><span data-ttu-id="708ca-103">Eigenschaften Blatt "Erweiterte Sicherheit"</span><span class="sxs-lookup"><span data-stu-id="708ca-103">Advanced Security Property Sheet</span></span>

<span data-ttu-id="708ca-104">Mithilfe des Eigenschaften Blatts erweiterte Sicherheit kann der Benutzer Bearbeitungsvorgänge ausführen, die auf der [Eigenschaften Seite grundlegende Sicherheit](basic-security-property-page.md) eines Zugriffs Steuerungs-Editors nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="708ca-104">The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor.</span></span> <span data-ttu-id="708ca-105">Das Eigenschaften Blatt kann die folgenden Eigenschaften Seiten enthalten:</span><span class="sxs-lookup"><span data-stu-id="708ca-105">The property sheet can include the following property pages:</span></span>

-   <span data-ttu-id="708ca-106">Eine [Berechtigungs](permissions-property-page.md) Eigenschaften Seite für die erweiterte Bearbeitung der [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts, z. b. das Bearbeiten [Objekt spezifischer ACEs](object-specific-aces.md) oder das Steuern der [ACE-Vererbung](ace-inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="708ca-106">A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).</span></span>
-   <span data-ttu-id="708ca-107">Eine [Eigenschaften](auditing-property-page.md) Seite für die Überwachung zum Anzeigen und Bearbeiten der [*System-Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) des Objekts.</span><span class="sxs-lookup"><span data-stu-id="708ca-107">An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span>
-   <span data-ttu-id="708ca-108">Eine Eigenschaften Seite des [Besitzers](owner-property-page.md) zum Ändern des Besitzers des Objekts.</span><span class="sxs-lookup"><span data-stu-id="708ca-108">An [Owner](owner-property-page.md) property page for changing the object's owner.</span></span>

<span data-ttu-id="708ca-109">Der Benutzer kann das Eigenschaften Blatt "Erweiterte Sicherheit" anzeigen, indem Sie auf der Eigenschaften Seite grundlegende Sicherheit auf die Schaltfläche **erweitert** klicken.</span><span class="sxs-lookup"><span data-stu-id="708ca-109">The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page.</span></span> <span data-ttu-id="708ca-110">Um die Schaltfläche **erweitert** anzuzeigen, legen Sie das Flag "Si \_ Advanced" in der Si-Objekt Informationsstruktur fest, die von Ihrer [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) -Implementierung zurückgegeben wurde. [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)</span><span class="sxs-lookup"><span data-stu-id="708ca-110">To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 

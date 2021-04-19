---
description: Eine NULL-DACL gewährt allen Benutzern, die Sie anfordert, vollen Zugriff. Eine leere DACL ist eine ordnungsgemäß zugewiesene und initialisierte DACL, die keine Zugriffs Steuerungs Einträge enthält. Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: Null-DACLs und leere DACLs (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364180"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a><span data-ttu-id="d2c84-105">Null-DACLs und leere DACLs (Autorisierung)</span><span class="sxs-lookup"><span data-stu-id="d2c84-105">Null DACLs and Empty DACLs (Authorization)</span></span>

<span data-ttu-id="d2c84-106">Wenn die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL), die zur [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) eines Objekts gehört, auf **null** festgelegt ist, wird eine NULL-DACL erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2c84-106">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that belongs to an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly) is set to **NULL**, a null DACL is created.</span></span> <span data-ttu-id="d2c84-107">Eine DACL mit NULL gewährt allen Benutzern Vollzugriff, die Sie anfordern. die normale Sicherheitsüberprüfung wird nicht in Bezug auf das-Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2c84-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="d2c84-108">Eine NULL-DACL darf nicht mit einer leeren DACL verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="d2c84-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="d2c84-109">Eine leere DACL ist eine ordnungsgemäß zugewiesene und initialisierte DACL, die keine [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) enthält.</span><span class="sxs-lookup"><span data-stu-id="d2c84-109">An empty DACL is a properly allocated and initialized DACL that contains no [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span> <span data-ttu-id="d2c84-110">Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d2c84-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="d2c84-111">Ein Beispiel für das Erstellen einer DACL finden Sie unter [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="d2c84-111">For an example of how to create a DACL, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

 

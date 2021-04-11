---
title: Null-DACLs und leere DACLs (AD DS)
description: Das vorhanden sein einer nicht freigegebenen Zugriffs Steuerungs Liste (DACL) im ntSecurityDescriptor-Attribut eines Objekts kann ein schwerwiegendes Sicherheitsrisiko darstellen.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Null DACLs und leere DACLs AD
- DACLs AD, NULL und leer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948554"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a><span data-ttu-id="39d9f-105">Null-DACLs und leere DACLs (AD DS)</span><span class="sxs-lookup"><span data-stu-id="39d9f-105">Null DACLs and Empty DACLs (AD DS)</span></span>

<span data-ttu-id="39d9f-106">Das vorhanden sein einer nicht freigegebenen Zugriffs Steuerungs Liste (DACL) im [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) -Attribut eines Objekts kann ein schwerwiegendes Sicherheitsrisiko darstellen.</span><span class="sxs-lookup"><span data-stu-id="39d9f-106">The presence of a null discretionary access-control list (DACL) in the [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) attribute of any object can create a serious security risk.</span></span> <span data-ttu-id="39d9f-107">Eine DACL mit NULL gewährt allen Benutzern Vollzugriff, die Sie anfordern. die normale Sicherheitsüberprüfung wird nicht in Bezug auf das-Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39d9f-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="39d9f-108">Eine NULL-DACL darf nicht mit einer leeren DACL verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="39d9f-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="39d9f-109">Eine leere DACL ist eine ordnungsgemäß zugewiesene und initialisierte DACL, die keine Zugriffs Steuerungs Einträge (ACEs) enthält.</span><span class="sxs-lookup"><span data-stu-id="39d9f-109">An empty DACL is a properly allocated and initialized DACL containing no access-control entries (ACEs).</span></span> <span data-ttu-id="39d9f-110">Eine leere DACL gewährt keinen Zugriff auf das Objekt, dem sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="39d9f-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="39d9f-111">Weitere Informationen finden Sie unter [null-DACLs und leere DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="39d9f-111">For more information, see [Null DACLs and Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span></span>

 

 
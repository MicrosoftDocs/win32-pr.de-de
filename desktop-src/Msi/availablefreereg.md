---
description: Die availablefreereg-Eigenschaft gibt in Kilobyte den gesamten freien Speicherplatz an, der in der Registrierung nach dem Aufrufen der Aktion "depjeeregistryspace" verfügbar ist. Der maximale Wert der availablefreereg-Eigenschaft beträgt 2 Millionen Kilobyte. Diese Eigenschaft wird nur unter Windows 2000 festgelegt.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Availablefreereg (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359680"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="bbdfb-103">Availablefreereg (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bbdfb-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="bbdfb-104">Die **availablefreereg** -Eigenschaft gibt in Kilobyte den gesamten freien Speicherplatz an, der in der Registrierung nach dem Aufrufen der [Aktion "depjeeregistryspace](allocateregistryspace-action.md)" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="bbdfb-105">Der maximale Wert der **availablefreereg** -Eigenschaft beträgt 2 Millionen Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="bbdfb-106">Diese Eigenschaft wird nur unter Windows 2000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbdfb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbdfb-107">Remarks</span></span>

<span data-ttu-id="bbdfb-108">Die **availablefreereg** -Eigenschaft muss auf einen Wert festgelegt werden, der groß genug ist, um für alle von der Installation hinzugefügten Registrierungsinformationen ausreichenden Speicherplatz in der Registrierung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="bbdfb-109">Der Mindestwert, der erforderlich ist, um ausreichend Speicherplatz sicherzustellen, hängt davon ab, wo sich die [Zuweisung "depasseregistryspace](allocateregistryspace-action.md) " in der Aktions Sequenz befindet, da der Installer beim Registrieren von Informationen in den Tabellen [Registry](registry-table.md), [Class](class-table.md), [selfreg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md)und [Verb](verb-table.md) automatisch den Speicherplatz vergrößert.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="bbdfb-110">Das Installationsprogramm erhöht den gesamten Registrierungsbereich nicht auf den durch **availablefreereg** angegebenen Betrag, bis "zustellereregistryspace" in der Aktions Sequenz erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="bbdfb-111">Wenn ' zugeregistryspace ' einer der ersten Aktionen in der Aktions Sequenz ist, sollte **availablefreereg** auf den gesamten Speicherplatz festgelegt werden, der für die Registrierungsinformationen in der Registrierungs Tabelle, der Klassen Tabelle, der TypeLib-Tabelle, der selfreg-Tabelle, der Erweiterungs Tabelle, der MIME-Tabelle, der Verb Tabelle, der Registrierung von [benutzerdefinierten Aktionen](custom-actions.md)</span><span class="sxs-lookup"><span data-stu-id="bbdfb-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="bbdfb-112">Der Wert von **availablefreereg** ist die Gesamtmenge der von der Installation hinzugefügten Informationen und stellt in allen Fällen ausreichend Speicherplatz zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="bbdfb-113">Dies ist auch der häufigste Fall.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-113">This is also the most common case.</span></span>

<span data-ttu-id="bbdfb-114">Wenn die Aktion "zuordnet zuregistrieren" in der Aktions Sequenz nach allen [Standard Aktionen](standard-actions.md) erstellt werden kann, die Registrierungsdaten schreiben, z. b. " [schreiteregistryvalues](writeregistryvalues-action.md) " und " [RegisterClassInfo](registerclassinfo-action.md)", muss der Wert von " **availablefreereg** " nur auf den Speicherplatz festgelegt werden, der zum Registrieren von benutzerdefinierten Aktionen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbdfb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbdfb-115">Requirements</span></span>



| <span data-ttu-id="bbdfb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbdfb-116">Requirement</span></span> | <span data-ttu-id="bbdfb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bbdfb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdfb-118">Version</span><span class="sxs-lookup"><span data-stu-id="bbdfb-118">Version</span></span><br/> | <span data-ttu-id="bbdfb-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bbdfb-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bbdfb-121">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bbdfb-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bbdfb-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bbdfb-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbdfb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbdfb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbdfb-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbdfb-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 





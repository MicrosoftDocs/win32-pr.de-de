---
title: Ireconcileinitiator-Schnittstelle
description: Macht Methoden verfügbar, die die Aktentasche-Auflösung mit der Möglichkeit bereitstellen, den Initiator über den Fortschritt zu benachrichtigen, ein Beendigungs Objekt festzulegen und eine bestimmte Version eines Dokuments anzufordern. Der Initiator ist für die Implementierung dieser Schnittstelle verantwortlich.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Ireconcileinitiator Interface Legacy Windows-Umgebungs Features
- Ireconcileinitiator Interface Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741600"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="62b4f-106">Ireconcileinitiator-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="62b4f-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="62b4f-107">Macht Methoden verfügbar, die die Aktentasche-Auflösung mit der Möglichkeit bereitstellen, den Initiator über den Fortschritt zu benachrichtigen, ein Beendigungs Objekt festzulegen und eine bestimmte Version eines Dokuments anzufordern.</span><span class="sxs-lookup"><span data-stu-id="62b4f-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="62b4f-108">Der Initiator ist für die Implementierung dieser Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="62b4f-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="62b4f-109">Member</span><span class="sxs-lookup"><span data-stu-id="62b4f-109">Members</span></span>

<span data-ttu-id="62b4f-110">Die **ireconcileinitiator** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="62b4f-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62b4f-111">**Ireconcileinitiator** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="62b4f-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="62b4f-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="62b4f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62b4f-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="62b4f-113">Methods</span></span>

<span data-ttu-id="62b4f-114">Die **ireconcileinitiator** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="62b4f-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="62b4f-115">Methode</span><span class="sxs-lookup"><span data-stu-id="62b4f-115">Method</span></span>                                                                 | <span data-ttu-id="62b4f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62b4f-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62b4f-117">**"-Tabortcallback"**</span><span class="sxs-lookup"><span data-stu-id="62b4f-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="62b4f-118">Legt das-Objekt fest, über das der Initiator eine Abstimmung asynchron beenden kann.</span><span class="sxs-lookup"><span data-stu-id="62b4f-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="62b4f-119">Bei einer Aktentasche-Synchronisierung wird dieses Objekt in der Regel für reversationen festgelegt, die langwierig sind oder eine Benutzerinteraktion umfassen.</span><span class="sxs-lookup"><span data-stu-id="62b4f-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="62b4f-120">**Setprogressfeedback**</span><span class="sxs-lookup"><span data-stu-id="62b4f-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="62b4f-121">Gibt den Fortschritt an, den der Aktentasche-Konflikt bei der ababstimmung durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="62b4f-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="62b4f-122">Der Betrag ist ein Bruchteil und wird als Quotienten der *ulprogress* -und *ulprogressmax* -Parameter berechnet.</span><span class="sxs-lookup"><span data-stu-id="62b4f-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="62b4f-123">Die Abstimmung sollte diese Methode in regelmäßigen Abständen während Ihres Abstimmungs Vorgangs aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="62b4f-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="62b4f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62b4f-124">Requirements</span></span>



| <span data-ttu-id="62b4f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62b4f-125">Requirement</span></span> | <span data-ttu-id="62b4f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="62b4f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b4f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62b4f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62b4f-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62b4f-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="62b4f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62b4f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62b4f-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62b4f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="62b4f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="62b4f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62b4f-132"><dt>Shell32.dll (Version 4,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="62b4f-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 


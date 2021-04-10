---
description: ACEs zum Steuern des Zugriffs auf Objekteigenschaften
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACEs zum Steuern des Zugriffs auf Objekteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215692"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="7ab2f-103">ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts</span><span class="sxs-lookup"><span data-stu-id="7ab2f-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="7ab2f-104">Die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines Verzeichnis Dienstanbieter (DS) kann wie folgt eine Hierarchie von [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) enthalten:</span><span class="sxs-lookup"><span data-stu-id="7ab2f-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="7ab2f-105">ACEs, die das Objekt selbst schützen</span><span class="sxs-lookup"><span data-stu-id="7ab2f-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="7ab2f-106">[Objektspezifische ACEs](object-specific-aces.md) , die eine angegebene Eigenschaft für das Objekt schützen</span><span class="sxs-lookup"><span data-stu-id="7ab2f-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="7ab2f-107">Objektspezifische ACEs, die eine angegebene Eigenschaft für das Objekt schützen</span><span class="sxs-lookup"><span data-stu-id="7ab2f-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="7ab2f-108">In dieser Hierarchie gelten die auf einer höheren Ebene gewährten oder verweigerten Rechte auch für die niedrigeren Ebenen.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="7ab2f-109">Wenn z. b. ein Objekt spezifischer ACE für einen Eigenschaften Satz einem Vertrauens nehmer ermöglicht, dass der Vertrauens nehmer für den Vertrauens nehmer über den \_ richtigen \_ \_ \_ Lesezugriff auf alle Eigenschaften dieses Eigenschaften Satzes verfügt, hat der Vertrauens nehmer impliziten Lesezugriff auf alle Eigenschaften dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="7ab2f-110">Analog dazu gewährt ein ACE für das Objekt selbst, das ADS den \_ rechten \_ DS \_ -Lesezugriff ermöglicht, den Vertrauens nehmer \_ Lesezugriff auf alle Eigenschaften des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="7ab2f-111">Die folgende Abbildung zeigt die Struktur eines hypothetischen DS-Objekts und seine Eigenschaften Sätze und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![Verzeichnisdienst-Objekthierarchie](images/accctrl2.png)

<span data-ttu-id="7ab2f-113">Angenommen, Sie möchten den folgenden Zugriff auf die Eigenschaften dieses DS-Objekts zulassen:</span><span class="sxs-lookup"><span data-stu-id="7ab2f-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="7ab2f-114">Berechtigung zum Lesen/Schreiben von Gruppen für alle Eigenschaften des Objekts zulassen</span><span class="sxs-lookup"><span data-stu-id="7ab2f-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="7ab2f-115">Lese-/Schreibberechtigung für alle anderen Eigenschaften mit Ausnahme von Eigenschaft D gestatten</span><span class="sxs-lookup"><span data-stu-id="7ab2f-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="7ab2f-116">Legen Sie hierzu die ACEs in der DACL des Objekts fest, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="7ab2f-117">Stiftungs</span><span class="sxs-lookup"><span data-stu-id="7ab2f-117">Trustee</span></span>  | <span data-ttu-id="7ab2f-118">Objekt-GUID</span><span class="sxs-lookup"><span data-stu-id="7ab2f-118">Object GUID</span></span>    | <span data-ttu-id="7ab2f-119">ACE-Typ</span><span class="sxs-lookup"><span data-stu-id="7ab2f-119">ACE type</span></span>                  | <span data-ttu-id="7ab2f-120">Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="7ab2f-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="7ab2f-121">Gruppe A</span><span class="sxs-lookup"><span data-stu-id="7ab2f-121">Group A</span></span>  | <span data-ttu-id="7ab2f-122">Keine</span><span class="sxs-lookup"><span data-stu-id="7ab2f-122">None</span></span>           | <span data-ttu-id="7ab2f-123">Zugriffs zulässiger ACE</span><span class="sxs-lookup"><span data-stu-id="7ab2f-123">Access-allowed ACE</span></span>        | <span data-ttu-id="7ab2f-124">ADS \_ right \_ DS \_ Read \_ Prop \| ADS \_ right \_ DS \_ Write \_ Prop</span><span class="sxs-lookup"><span data-stu-id="7ab2f-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="7ab2f-125">Jeder</span><span class="sxs-lookup"><span data-stu-id="7ab2f-125">Everyone</span></span> | <span data-ttu-id="7ab2f-126">Eigenschaften Satz 1</span><span class="sxs-lookup"><span data-stu-id="7ab2f-126">Property Set 1</span></span> | <span data-ttu-id="7ab2f-127">Zugriffs zulässiger Objekt-ACE</span><span class="sxs-lookup"><span data-stu-id="7ab2f-127">Access-allowed object ACE</span></span> | <span data-ttu-id="7ab2f-128">ADS \_ right \_ DS \_ Read \_ Prop \| ADS \_ right \_ DS \_ Write \_ Prop</span><span class="sxs-lookup"><span data-stu-id="7ab2f-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="7ab2f-129">Jeder</span><span class="sxs-lookup"><span data-stu-id="7ab2f-129">Everyone</span></span> | <span data-ttu-id="7ab2f-130">Eigenschaft C</span><span class="sxs-lookup"><span data-stu-id="7ab2f-130">Property C</span></span>     | <span data-ttu-id="7ab2f-131">Zugriffs zulässiger Objekt-ACE</span><span class="sxs-lookup"><span data-stu-id="7ab2f-131">Access-allowed object ACE</span></span> | <span data-ttu-id="7ab2f-132">ADS \_ right \_ DS \_ Read \_ Prop \| ADS \_ right \_ DS \_ Write \_ Prop</span><span class="sxs-lookup"><span data-stu-id="7ab2f-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="7ab2f-133">Der ACE für Gruppe A weist keine Objekt-GUID auf, was bedeutet, dass er den Zugriff auf alle Eigenschaften des Objekts zulässt.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="7ab2f-134">Der objektspezifische ACE für den Eigenschaften Satz 1 ermöglicht allen Benutzern den Zugriff auf die Eigenschaften A und B. Der andere objektspezifische ACE ermöglicht allen Benutzern den Zugriff auf die Eigenschaft C. Beachten Sie, dass diese DACL zwar keine Zugriffs verweigerten ACEs hat, aber den Zugriff auf die Eigenschaft D für alle außer Gruppe A implizit verweigert.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="7ab2f-135">Wenn ein Benutzer versucht, auf die-Eigenschaft eines Objekts zuzugreifen, überprüft das System die ACEs in der angegebenen Reihenfolge, bis der angeforderte Zugriff explizit gewährt, verweigert wird oder keine weiteren ACEs vorhanden sind. in diesem Fall wird der Zugriff implizit verweigert.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="7ab2f-136">Das System wertet Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7ab2f-136">The system evaluates:</span></span>

-   <span data-ttu-id="7ab2f-137">ACEs, die auf das Objekt selbst angewendet werden</span><span class="sxs-lookup"><span data-stu-id="7ab2f-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="7ab2f-138">Objektspezifische ACEs, die auf den Eigenschaften Satz angewendet werden, der die Eigenschaft enthält, auf die zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="7ab2f-139">Objektspezifische ACEs, die auf die Eigenschaft angewendet werden, auf die zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="7ab2f-140">Das System ignoriert objektspezifische ACEs, die auf andere Eigenschaften Sätze oder Eigenschaften angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ab2f-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 

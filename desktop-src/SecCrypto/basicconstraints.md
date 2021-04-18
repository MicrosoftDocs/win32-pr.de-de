---
description: Stellt die grundlegende Einschränkungs Erweiterung eines Zertifikats dar.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Basiceinschränkungs-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358699"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="ffea0-103">Basiceinschränkungs-Objekt</span><span class="sxs-lookup"><span data-stu-id="ffea0-103">BasicConstraints object</span></span>

<span data-ttu-id="ffea0-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffea0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="ffea0-105">Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ffea0-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="ffea0-106">Das **basiceinschränkunsobjekt** stellt die grundlegende Einschränkungs Erweiterung eines Zertifikats dar.</span><span class="sxs-lookup"><span data-stu-id="ffea0-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ffea0-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="ffea0-107">When to use</span></span>

<span data-ttu-id="ffea0-108">Das **basiceinschränkungs** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="ffea0-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="ffea0-109">Bestimmen Sie, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ffea0-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="ffea0-110">Bestimmen Sie, ob die Erweiterung für Basis Einschränkungen als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ffea0-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="ffea0-111">Bestimmen Sie, ob das Zertifikat auf Zertifizierungsstellen beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="ffea0-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="ffea0-112">Bestimmen Sie, ob die Einschränkung der Pfadlänge vorhanden ist, und rufen Sie den Einschränkungs Wert der Pfadlänge ab</span><span class="sxs-lookup"><span data-stu-id="ffea0-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="ffea0-113">Member</span><span class="sxs-lookup"><span data-stu-id="ffea0-113">Members</span></span>

<span data-ttu-id="ffea0-114">Das **basiceinschränkungs** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ffea0-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="ffea0-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffea0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffea0-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffea0-116">Properties</span></span>

<span data-ttu-id="ffea0-117">Das **basiceinschränkungs** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ffea0-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="ffea0-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ffea0-118">Property</span></span>                                                                                     | <span data-ttu-id="ffea0-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ffea0-119">Access type</span></span>          | <span data-ttu-id="ffea0-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffea0-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffea0-121">**Iscertificateauthority**</span><span class="sxs-lookup"><span data-stu-id="ffea0-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="ffea0-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffea0-122">Read-only</span></span><br/> | <span data-ttu-id="ffea0-123">Ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) gilt.</span><span class="sxs-lookup"><span data-stu-id="ffea0-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="ffea0-124">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="ffea0-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="ffea0-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffea0-125">Read-only</span></span><br/> | <span data-ttu-id="ffea0-126">Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ffea0-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="ffea0-127">**Ispathlenbeschränintpresent**</span><span class="sxs-lookup"><span data-stu-id="ffea0-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="ffea0-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffea0-128">Read-only</span></span><br/> | <span data-ttu-id="ffea0-129">Ruft einen booleschen Wert ab, der angibt, ob die Pfadlängen Einschränkung des Zertifikats vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ffea0-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="ffea0-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="ffea0-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="ffea0-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffea0-131">Read-only</span></span><br/> | <span data-ttu-id="ffea0-132">Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ffea0-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="ffea0-133">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ffea0-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="ffea0-134">**PathLenConstraint**</span><span class="sxs-lookup"><span data-stu-id="ffea0-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="ffea0-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffea0-135">Read-only</span></span><br/> | <span data-ttu-id="ffea0-136">Ruft den Wert der Path-Längen Einschränkung ab.</span><span class="sxs-lookup"><span data-stu-id="ffea0-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ffea0-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffea0-137">Remarks</span></span>

<span data-ttu-id="ffea0-138">Das **basiceinschränkunsobjekt** kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ffea0-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffea0-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffea0-139">Requirements</span></span>



| <span data-ttu-id="ffea0-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffea0-140">Requirement</span></span> | <span data-ttu-id="ffea0-141">Wert</span><span class="sxs-lookup"><span data-stu-id="ffea0-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffea0-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ffea0-142">End of client support</span></span><br/> | <span data-ttu-id="ffea0-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffea0-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ffea0-144">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ffea0-144">End of server support</span></span><br/> | <span data-ttu-id="ffea0-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffea0-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ffea0-146">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ffea0-146">Redistributable</span></span><br/>       | <span data-ttu-id="ffea0-147">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ffea0-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ffea0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ffea0-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ffea0-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffea0-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffea0-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffea0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffea0-151">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="ffea0-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

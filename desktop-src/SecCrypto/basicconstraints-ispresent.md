---
description: Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung vorhanden ist. Dies ist die Standard Eigenschaft.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: Basiceinschränkungs. ispree sent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370670"
---
# <a name="basicconstraintsispresent-property"></a><span data-ttu-id="6400e-104">Basiceinschränkungs. ispree sent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6400e-104">BasicConstraints.IsPresent property</span></span>

<span data-ttu-id="6400e-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6400e-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="6400e-106">Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="6400e-106">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="6400e-107">Die **ispree sent** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6400e-107">The **IsPresent** property retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="6400e-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6400e-108">This is the default property.</span></span>

<span data-ttu-id="6400e-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6400e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6400e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6400e-110">Syntax</span></span>


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6400e-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6400e-111">Property value</span></span>

<span data-ttu-id="6400e-112">**True** gibt an, dass die grundlegende Einschränkungs Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6400e-112">If **true**, the basic constraints extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="6400e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6400e-113">Requirements</span></span>



| <span data-ttu-id="6400e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6400e-114">Requirement</span></span> | <span data-ttu-id="6400e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6400e-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6400e-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6400e-116">End of client support</span></span><br/> | <span data-ttu-id="6400e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6400e-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6400e-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6400e-118">End of server support</span></span><br/> | <span data-ttu-id="6400e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6400e-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6400e-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6400e-120">Redistributable</span></span><br/>       | <span data-ttu-id="6400e-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6400e-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6400e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6400e-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6400e-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6400e-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6400e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6400e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6400e-125">**Basiceinschränkungen**</span><span class="sxs-lookup"><span data-stu-id="6400e-125">**BasicConstraints**</span></span>](basicconstraints.md)
</dt> </dl>

 

 

---
description: Ruft einen booleschen Wert ab, der angibt, ob die Einschränkung der Pfadlänge vorhanden ist.
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: Basiceinschränkungs. ispathlenbeschränintpresent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9809b6747bac548b14b37384719dbe2660188582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370069"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a><span data-ttu-id="ab651-103">Basiceinschränkungs. ispathlenbeschränintpresent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab651-103">BasicConstraints.IsPathLenConstraintPresent property</span></span>

<span data-ttu-id="ab651-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab651-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="ab651-105">Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ab651-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="ab651-106">Die **ispathleneinschränintpresent** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Einschränkung der Pfadlänge vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ab651-106">The **IsPathLenConstraintPresent** property retrieves a Boolean value that indicates whether the path length constraint is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab651-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab651-107">Syntax</span></span>


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ab651-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ab651-108">Property value</span></span>

<span data-ttu-id="ab651-109">**True** gibt an, dass die Einschränkung der Pfadlänge vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ab651-109">If **True**, the path length constraint is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab651-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab651-110">Requirements</span></span>



| <span data-ttu-id="ab651-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab651-111">Requirement</span></span> | <span data-ttu-id="ab651-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ab651-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab651-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ab651-113">End of client support</span></span><br/> | <span data-ttu-id="ab651-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab651-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ab651-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ab651-115">End of server support</span></span><br/> | <span data-ttu-id="ab651-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab651-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ab651-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ab651-117">Redistributable</span></span><br/>       | <span data-ttu-id="ab651-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab651-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ab651-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ab651-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ab651-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab651-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

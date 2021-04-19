---
description: Ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung als kritisch markiert ist.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Basiceinschränkungs. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361408"
---
# <a name="basicconstraintsiscritical-property"></a><span data-ttu-id="821b8-103">Basiceinschränkungs. IsCritical (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="821b8-103">BasicConstraints.IsCritical property</span></span>

<span data-ttu-id="821b8-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="821b8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="821b8-105">Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="821b8-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="821b8-106">Die **IsCritical** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die grundlegende Einschränkungs Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="821b8-106">The **IsCritical** property retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span>

<span data-ttu-id="821b8-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="821b8-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="821b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="821b8-108">Syntax</span></span>


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="821b8-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="821b8-109">Property value</span></span>

<span data-ttu-id="821b8-110">**True** gibt an, dass die grundlegende Einschränkungs Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="821b8-110">If **true**, the basic constraint extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="821b8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="821b8-111">Requirements</span></span>



| <span data-ttu-id="821b8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="821b8-112">Requirement</span></span> | <span data-ttu-id="821b8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="821b8-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="821b8-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="821b8-114">End of client support</span></span><br/> | <span data-ttu-id="821b8-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="821b8-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="821b8-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="821b8-116">End of server support</span></span><br/> | <span data-ttu-id="821b8-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="821b8-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="821b8-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="821b8-118">Redistributable</span></span><br/>       | <span data-ttu-id="821b8-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="821b8-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="821b8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="821b8-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="821b8-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="821b8-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

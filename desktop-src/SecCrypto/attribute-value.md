---
description: Legt den Wert des Attributs fest oder ruft ihn ab.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute. Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361611"
---
# <a name="attributevalue-property"></a><span data-ttu-id="33b8a-103">Attribute. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33b8a-103">Attribute.Value property</span></span>

<span data-ttu-id="33b8a-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="33b8a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="33b8a-105">Verwenden Sie stattdessen die [**cryptographiertributeobject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="33b8a-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="33b8a-106">Die **value** -Eigenschaft legt den Wert des Attributs fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="33b8a-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="33b8a-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="33b8a-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="33b8a-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="33b8a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="33b8a-109">Property value</span></span>

<span data-ttu-id="33b8a-110">Eine **Variant** -Variable, die den Wert des Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="33b8a-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="33b8a-111">Für **\_ authentifizierte CAPICOM \_ Attribute \_ SIGNING \_ time** -Attribute ist der Datentyp **Date**.</span><span class="sxs-lookup"><span data-stu-id="33b8a-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="33b8a-112">Für alle anderen Attribute ist der Eigenschafts Wert eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="33b8a-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b8a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33b8a-113">Requirements</span></span>



| <span data-ttu-id="33b8a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b8a-114">Requirement</span></span> | <span data-ttu-id="33b8a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="33b8a-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33b8a-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="33b8a-116">End of client support</span></span><br/> | <span data-ttu-id="33b8a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33b8a-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="33b8a-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="33b8a-118">End of server support</span></span><br/> | <span data-ttu-id="33b8a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33b8a-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="33b8a-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="33b8a-120">Redistributable</span></span><br/>       | <span data-ttu-id="33b8a-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="33b8a-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="33b8a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="33b8a-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="33b8a-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b8a-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

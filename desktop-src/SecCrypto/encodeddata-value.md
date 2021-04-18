---
description: Ruft die codierten Daten ab.
ms.assetid: 8e07ac14-6859-410f-ab30-84b8d60a94ad
title: Encoddata. Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e040f78d5c0ccfa3e50729f16b75a0691771980e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365819"
---
# <a name="encodeddatavalue-property"></a><span data-ttu-id="f7340-103">Encoddata. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7340-103">EncodedData.Value property</span></span>

<span data-ttu-id="f7340-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7340-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f7340-105">Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f7340-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f7340-106">Mit der **value** -Eigenschaft werden die codierten Daten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f7340-106">The **Value** property retrieves the encoded data.</span></span> <span data-ttu-id="f7340-107">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f7340-107">This is the default property.</span></span>

<span data-ttu-id="f7340-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f7340-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7340-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7340-109">Syntax</span></span>


```VB
EncodedData.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="f7340-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f7340-110">Property value</span></span>

<span data-ttu-id="f7340-111">Eine Zeichenfolge, die die codierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f7340-111">A string that contains the encoded data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7340-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7340-112">Requirements</span></span>



| <span data-ttu-id="f7340-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7340-113">Requirement</span></span> | <span data-ttu-id="f7340-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f7340-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7340-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f7340-115">End of client support</span></span><br/> | <span data-ttu-id="f7340-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7340-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7340-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f7340-117">End of server support</span></span><br/> | <span data-ttu-id="f7340-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7340-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7340-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f7340-119">Redistributable</span></span><br/>       | <span data-ttu-id="f7340-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7340-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7340-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f7340-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f7340-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7340-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

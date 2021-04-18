---
description: Die Item-Eigenschaft ruft ein ExtendedProperty-Objekt aus der Auflistung ab. Dies ist die Standard Eigenschaft.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: ExtendedProperties. Item (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372422"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="f5ac2-104">ExtendedProperties. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f5ac2-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="f5ac2-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5ac2-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f5ac2-106">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5ac2-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="f5ac2-107">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5ac2-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f5ac2-108">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="f5ac2-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f5ac2-109">Die **Item** -Eigenschaft ruft ein [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f5ac2-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="f5ac2-110">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f5ac2-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ac2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5ac2-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="f5ac2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f5ac2-112">Property value</span></span>

<span data-ttu-id="f5ac2-113">Ein [**ExtendedProperty**](extendedproperty.md) -Objekt, das die indizierte erweiterte Eigenschaft der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5ac2-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ac2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5ac2-114">Requirements</span></span>



| <span data-ttu-id="f5ac2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5ac2-115">Requirement</span></span> | <span data-ttu-id="f5ac2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f5ac2-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ac2-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f5ac2-117">End of client support</span></span><br/> | <span data-ttu-id="f5ac2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5ac2-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f5ac2-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f5ac2-119">End of server support</span></span><br/> | <span data-ttu-id="f5ac2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5ac2-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f5ac2-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f5ac2-121">Redistributable</span></span><br/>       | <span data-ttu-id="f5ac2-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5ac2-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f5ac2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f5ac2-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f5ac2-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5ac2-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

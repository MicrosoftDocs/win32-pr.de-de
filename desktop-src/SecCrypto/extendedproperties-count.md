---
description: Ruft die Anzahl von ExtendedProperty-Objekten in der-Auflistung ab.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: ExtendedProperties. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365469"
---
# <a name="extendedpropertiescount-property"></a><span data-ttu-id="f7cd4-103">ExtendedProperties. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7cd4-103">ExtendedProperties.Count property</span></span>

<span data-ttu-id="f7cd4-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f7cd4-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="f7cd4-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7cd4-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f7cd4-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="f7cd4-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f7cd4-108">Die **count** -Eigenschaft ruft die Anzahl von [**ExtendedProperty**](extendedproperty.md) -Objekten in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-108">The **Count** property retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cd4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7cd4-109">Syntax</span></span>


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="f7cd4-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f7cd4-110">Property value</span></span>

<span data-ttu-id="f7cd4-111">Die Anzahl von [**ExtendedProperty**](extendedproperty.md) -Objekten in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-111">The number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7cd4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7cd4-112">Requirements</span></span>



| <span data-ttu-id="f7cd4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7cd4-113">Requirement</span></span> | <span data-ttu-id="f7cd4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f7cd4-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7cd4-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f7cd4-115">End of client support</span></span><br/> | <span data-ttu-id="f7cd4-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7cd4-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7cd4-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f7cd4-117">End of server support</span></span><br/> | <span data-ttu-id="f7cd4-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7cd4-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7cd4-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f7cd4-119">Redistributable</span></span><br/>       | <span data-ttu-id="f7cd4-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7cd4-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7cd4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f7cd4-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f7cd4-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7cd4-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

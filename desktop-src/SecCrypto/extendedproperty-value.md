---
description: Legt die erweiterten Eigenschaften Daten fest oder ruft Sie ab.
ms.assetid: 115bb52a-e64d-4d84-a491-35f6dba25a58
title: ExtendedProperty. Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ebbd977a107d92661110ceff02f3a5bb0bea191e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371987"
---
# <a name="extendedpropertyvalue-property"></a><span data-ttu-id="9cde0-103">ExtendedProperty. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9cde0-103">ExtendedProperty.Value property</span></span>

<span data-ttu-id="9cde0-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9cde0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9cde0-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9cde0-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="9cde0-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="9cde0-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="9cde0-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="9cde0-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="9cde0-108">Die **value** -Eigenschaft legt die erweiterten Eigenschaften Daten fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="9cde0-108">The **Value** property sets or retrieves the extended property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cde0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cde0-109">Syntax</span></span>


```VB
ExtendedProperty.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="9cde0-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9cde0-110">Property value</span></span>

<span data-ttu-id="9cde0-111">Die erweiterten Eigenschaften Daten in dem von *EncodingType* angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="9cde0-111">The extended property data, in the format specified by *EncodingType*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cde0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cde0-112">Requirements</span></span>



| <span data-ttu-id="9cde0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cde0-113">Requirement</span></span> | <span data-ttu-id="9cde0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9cde0-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cde0-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9cde0-115">End of client support</span></span><br/> | <span data-ttu-id="9cde0-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cde0-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9cde0-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9cde0-117">End of server support</span></span><br/> | <span data-ttu-id="9cde0-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cde0-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9cde0-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9cde0-119">Redistributable</span></span><br/>       | <span data-ttu-id="9cde0-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="9cde0-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9cde0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9cde0-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9cde0-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cde0-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

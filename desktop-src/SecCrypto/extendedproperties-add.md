---
description: Fügt der Auflistung eine erweiterte Eigenschaft hinzu.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: ExtendedProperties. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360918"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="cf836-103">ExtendedProperties. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="cf836-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="cf836-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf836-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cf836-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cf836-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="cf836-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf836-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="cf836-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="cf836-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="cf836-108">Durch die **Add** -Methode wird der Auflistung eine erweiterte Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cf836-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf836-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf836-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="cf836-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf836-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf836-111">*valproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf836-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf836-112">Ein [**ExtendedProperty**](extendedproperty.md) -Objekt, das die erweiterte Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="cf836-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf836-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf836-113">Return value</span></span>

<span data-ttu-id="cf836-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cf836-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf836-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf836-115">Requirements</span></span>



| <span data-ttu-id="cf836-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf836-116">Requirement</span></span> | <span data-ttu-id="cf836-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cf836-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf836-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cf836-118">End of client support</span></span><br/> | <span data-ttu-id="cf836-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf836-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cf836-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cf836-120">End of server support</span></span><br/> | <span data-ttu-id="cf836-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf836-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cf836-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cf836-122">Redistributable</span></span><br/>       | <span data-ttu-id="cf836-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf836-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cf836-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cf836-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cf836-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf836-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

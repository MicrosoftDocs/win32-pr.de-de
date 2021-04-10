---
description: Eine Rückruffunktion, mit der der Host darüber benachrichtigt wird, welche Schnittstellen unterstützt werden.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iversioncallback:: versiontableready-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124693"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="aed51-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>Iversioncallback:: versiontableready-Methode</span><span class="sxs-lookup"><span data-stu-id="aed51-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="aed51-104">Eine Rückruffunktion, mit der der Host darüber benachrichtigt wird, welche Schnittstellen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="aed51-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed51-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aed51-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="aed51-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aed51-106">Parameters</span></span>

<span data-ttu-id="aed51-107">*count1- \_ interfakeids* </span><span class="sxs-lookup"><span data-stu-id="aed51-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="aed51-108">Ein Array, das die GUIDs unterstützter Schnittstellen-IDs enthält.</span><span class="sxs-lookup"><span data-stu-id="aed51-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="aed51-109">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="aed51-109">*count* </span></span>  
<span data-ttu-id="aed51-110">Die Anzahl der GUIDs, die in count1- \_ interfakeids übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="aed51-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="aed51-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aed51-111">Return value</span></span>

<span data-ttu-id="aed51-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="aed51-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aed51-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aed51-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aed51-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aed51-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aed51-115">Header</span><span class="sxs-lookup"><span data-stu-id="aed51-115">Header</span></span></p></td><td><span data-ttu-id="aed51-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aed51-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aed51-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aed51-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aed51-118">**Iversioncallback**</span><span class="sxs-lookup"><span data-stu-id="aed51-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 

---
description: Ruft den Bezeichner des Diensts ab, der mit dem Endpunkt Token authentifiziert werden soll.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Iupdateendpointauthtoken:: serviceid-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359863"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="77541-103">Iupdateendpointauthtoken:: serviceid-Methode</span><span class="sxs-lookup"><span data-stu-id="77541-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="77541-104">Ruft den Bezeichner des Diensts ab, der mit dem Endpunkt Token authentifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="77541-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="77541-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77541-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="77541-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77541-107">*pserviceid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="77541-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77541-108">Der Bezeichner des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="77541-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77541-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77541-109">Return value</span></span>

<span data-ttu-id="77541-110">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="77541-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="77541-111">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77541-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="77541-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77541-112">Requirements</span></span>



| <span data-ttu-id="77541-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77541-113">Requirement</span></span> | <span data-ttu-id="77541-114">Wert</span><span class="sxs-lookup"><span data-stu-id="77541-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77541-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77541-115">Minimum supported client</span></span><br/> | <span data-ttu-id="77541-116">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77541-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="77541-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77541-117">Minimum supported server</span></span><br/> | <span data-ttu-id="77541-118">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77541-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="77541-119">Header</span><span class="sxs-lookup"><span data-stu-id="77541-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="77541-120"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="77541-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="77541-121">IDL</span><span class="sxs-lookup"><span data-stu-id="77541-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77541-122"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77541-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="77541-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77541-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="77541-124"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77541-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="77541-125">DLL</span><span class="sxs-lookup"><span data-stu-id="77541-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77541-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77541-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77541-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77541-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77541-128">**Iupdateendpointauthtoken**</span><span class="sxs-lookup"><span data-stu-id="77541-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 





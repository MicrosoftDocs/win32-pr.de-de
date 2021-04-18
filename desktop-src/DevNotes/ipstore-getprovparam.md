---
description: Dient zum Festlegen der angegebenen Parameterinformationen.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Ipstore:: getprovparam-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359225"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="621d2-103">Ipstore:: getprovparam-Methode</span><span class="sxs-lookup"><span data-stu-id="621d2-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="621d2-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="621d2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="621d2-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="621d2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="621d2-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="621d2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="621d2-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="621d2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="621d2-108">\[Diese Methode ist nicht implementiert.\]</span><span class="sxs-lookup"><span data-stu-id="621d2-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="621d2-109">Dient zum Festlegen der angegebenen Parameterinformationen.</span><span class="sxs-lookup"><span data-stu-id="621d2-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="621d2-110">Beachten Sie jedoch, dass Sie nicht implementiert wird und immer fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="621d2-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="621d2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="621d2-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="621d2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="621d2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="621d2-113">*dwparam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="621d2-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="621d2-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="621d2-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="621d2-115">*pcbData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="621d2-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="621d2-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="621d2-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="621d2-117">*ppbdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="621d2-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="621d2-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="621d2-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="621d2-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="621d2-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="621d2-120">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="621d2-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="621d2-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="621d2-121">Return value</span></span>

<span data-ttu-id="621d2-122">Bei Aufrufen dieser Methode tritt immer ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="621d2-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="621d2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="621d2-123">Requirements</span></span>



| <span data-ttu-id="621d2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="621d2-124">Requirement</span></span> | <span data-ttu-id="621d2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="621d2-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="621d2-126">Header</span><span class="sxs-lookup"><span data-stu-id="621d2-126">Header</span></span><br/> | <dl> <span data-ttu-id="621d2-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="621d2-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="621d2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="621d2-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="621d2-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="621d2-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621d2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="621d2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621d2-131">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="621d2-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 

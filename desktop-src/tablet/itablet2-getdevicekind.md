---
description: Gibt den Typ des Hardware Geräts zurück, das das Tablet-Objekt darstellt, z. b. Maus, Stift oder Fingereingabe
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'ITablet2:: getdevicekind-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359130"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="403c3-103">ITablet2:: getdevicekind-Methode</span><span class="sxs-lookup"><span data-stu-id="403c3-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="403c3-104">Gibt den Typ des Hardware Geräts zurück, das das Tablet-Objekt darstellt, z. b. Maus, Stift oder Fingereingabe</span><span class="sxs-lookup"><span data-stu-id="403c3-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="403c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="403c3-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="403c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="403c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403c3-107">*pkind* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="403c3-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="403c3-108">-Enumerationswert, der den Typ des Tablets angibt, z. b. Maus, Stift oder Fingereingabe.</span><span class="sxs-lookup"><span data-stu-id="403c3-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403c3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="403c3-109">Return value</span></span>

<span data-ttu-id="403c3-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="403c3-110">This method can return one of these values.</span></span>



| <span data-ttu-id="403c3-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="403c3-111">Return code</span></span>                                                                            | <span data-ttu-id="403c3-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="403c3-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="403c3-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="403c3-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="403c3-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="403c3-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="403c3-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="403c3-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="403c3-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="403c3-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="403c3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="403c3-117">Remarks</span></span>

<span data-ttu-id="403c3-118">Diese Schnittstelle und Methode wurden in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="403c3-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="403c3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="403c3-119">Requirements</span></span>



| <span data-ttu-id="403c3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="403c3-120">Requirement</span></span> | <span data-ttu-id="403c3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="403c3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="403c3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="403c3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="403c3-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="403c3-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="403c3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="403c3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="403c3-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="403c3-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="403c3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="403c3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="403c3-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="403c3-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="403c3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="403c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403c3-129">**ITablet2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="403c3-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="403c3-130">**Tablet \_ Device \_ Kind-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="403c3-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="403c3-131">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="403c3-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 





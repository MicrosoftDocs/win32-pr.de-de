---
description: Ruft den eindeutigen Bezeichner der Tablettstiftschaltfläche ab.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'Itabletcurrsorbutton:: GetGuid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042717"
---
# <a name="itabletcursorbuttongetguid-method"></a><span data-ttu-id="0dd0e-103">Itabletcurrsorbutton:: GetGuid-Methode</span><span class="sxs-lookup"><span data-stu-id="0dd0e-103">ITabletCursorButton::GetGuid method</span></span>

<span data-ttu-id="0dd0e-104">Ruft den eindeutigen Bezeichner der Tablettstiftschaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="0dd0e-104">Retrieves the unique identifier of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dd0e-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a><span data-ttu-id="0dd0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dd0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd0e-107">*pguidbtn* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0dd0e-107">*pguidBtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd0e-108">Ein eindeutiger Wert, der die Tablettstiftschaltfläche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0dd0e-108">A unique value that identifies the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd0e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0dd0e-109">Return value</span></span>

<span data-ttu-id="0dd0e-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0dd0e-110">This method can return one of these values.</span></span>



| <span data-ttu-id="0dd0e-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0dd0e-111">Return code</span></span>                                                                            | <span data-ttu-id="0dd0e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dd0e-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0dd0e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0dd0e-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0dd0e-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0dd0e-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0dd0e-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="0dd0e-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0dd0e-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0dd0e-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0dd0e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dd0e-117">Requirements</span></span>



| <span data-ttu-id="0dd0e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dd0e-118">Requirement</span></span> | <span data-ttu-id="0dd0e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0dd0e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd0e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0dd0e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0dd0e-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0dd0e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0dd0e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0dd0e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0dd0e-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0dd0e-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0dd0e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0dd0e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0dd0e-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0dd0e-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd0e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd0e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd0e-127">**Itabletcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0dd0e-127">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 





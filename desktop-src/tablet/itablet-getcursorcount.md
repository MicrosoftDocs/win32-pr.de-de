---
description: Gibt die Anzahl der dem Tablet zugeordneten Cursor Objekte zurück.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'ITablet:: getcurrsorcount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352493"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="25f70-103">ITablet:: getcurrsorcount-Methode</span><span class="sxs-lookup"><span data-stu-id="25f70-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="25f70-104">Gibt die Anzahl der dem Tablet zugeordneten Cursor Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="25f70-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25f70-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="25f70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f70-107">*pccurrs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25f70-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25f70-108">Die Anzahl der dem Tablet zugeordneten Cursor Objekte.</span><span class="sxs-lookup"><span data-stu-id="25f70-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f70-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25f70-109">Return value</span></span>

<span data-ttu-id="25f70-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="25f70-110">This method can return one of these values.</span></span>



| <span data-ttu-id="25f70-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="25f70-111">Return code</span></span>                                                                            | <span data-ttu-id="25f70-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25f70-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="25f70-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25f70-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="25f70-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="25f70-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="25f70-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="25f70-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="25f70-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="25f70-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25f70-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25f70-117">Requirements</span></span>



| <span data-ttu-id="25f70-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25f70-118">Requirement</span></span> | <span data-ttu-id="25f70-119">Wert</span><span class="sxs-lookup"><span data-stu-id="25f70-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f70-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25f70-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25f70-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25f70-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25f70-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25f70-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25f70-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="25f70-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="25f70-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25f70-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="25f70-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25f70-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f70-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25f70-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f70-127">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="25f70-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 





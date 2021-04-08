---
title: ImageList_SetColorTable-Funktion
description: Legt die Farbtabelle für eine Bildliste fest.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Windows-Steuerelemente ImageList_SetColorTable-Funktion
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957268"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="cb556-104">ImageList- \_ setcolortable-Funktion</span><span class="sxs-lookup"><span data-stu-id="cb556-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="cb556-105">Legt die Farbtabelle für eine Bildliste fest.</span><span class="sxs-lookup"><span data-stu-id="cb556-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb556-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb556-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="cb556-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb556-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb556-108">*HIML* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb556-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb556-109">Typ: **HIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="cb556-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="cb556-110">Ein Handle für die Bildliste.</span><span class="sxs-lookup"><span data-stu-id="cb556-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="cb556-111">*starten* \[ Sie in\]</span><span class="sxs-lookup"><span data-stu-id="cb556-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb556-112">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="cb556-112">Type: **int**</span></span>

<span data-ttu-id="cb556-113">Ein NULL basierter Index der Farbtabelle, der den ersten festzulegenden Farb Tabelleneintrag angibt.</span><span class="sxs-lookup"><span data-stu-id="cb556-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="cb556-114">*len* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb556-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb556-115">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="cb556-115">Type: **int**</span></span>

<span data-ttu-id="cb556-116">Die Anzahl der festzulegenden farbtabelleneinträge.</span><span class="sxs-lookup"><span data-stu-id="cb556-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="cb556-117">*prgb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb556-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb556-118">Typ: \**[**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="cb556-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="cb556-119">Ein Zeiger auf ein Array von _Len \* [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen, das neue Farbinformationen für die Farbtabelle der DIB enthält.</span><span class="sxs-lookup"><span data-stu-id="cb556-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb556-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb556-120">Return value</span></span>

<span data-ttu-id="cb556-121">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="cb556-121">Type: **int**</span></span>

<span data-ttu-id="cb556-122">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie die Anzahl der farbtabelleneinträge zurück, die von der Funktion festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb556-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="cb556-123">Wenn die Funktion fehlschlägt, ist der Rückgabewert kleiner oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cb556-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb556-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb556-124">Remarks</span></span>

<span data-ttu-id="cb556-125">Nur Bildlisten, die mit dem [**ILC- \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) -oder [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) -Flag erstellt wurden, haben Farbtabellen.</span><span class="sxs-lookup"><span data-stu-id="cb556-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="cb556-126">Die Farbtabelle einer solchen Bildliste wird in der Regel automatisch festgelegt, indem die Farbtabelle des ersten Bilds kopiert wird, das der Liste hinzugefügt wird (z. b. über die Funktion " [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) "), wenn dieses Bild ein DIB ist.</span><span class="sxs-lookup"><span data-stu-id="cb556-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="cb556-127">Wenn das erste der Bildliste hinzugefügte Bild kein DIB ist, dann wird die Farbtabelle der Halbton-Palette für **ILC- \_ COLOR8** -Bildlisten und die VGA-Farbtabelle für **ILC- \_ COLOR4** verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb556-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb556-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb556-128">Requirements</span></span>



| <span data-ttu-id="cb556-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb556-129">Requirement</span></span> | <span data-ttu-id="cb556-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cb556-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb556-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb556-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cb556-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb556-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="cb556-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb556-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cb556-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb556-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cb556-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cb556-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb556-136"><dt>Comctl32.dll (Version 3,51 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cb556-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb556-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb556-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb556-138">[Farbtabelle](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="cb556-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 


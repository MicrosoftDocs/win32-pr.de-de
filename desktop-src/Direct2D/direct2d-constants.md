---
title: Direct2D-Konstanten
description: Direct2D definiert die folgende Liste von Konstanten.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343864"
---
# <a name="direct2d-constants"></a><span data-ttu-id="b4222-103">Direct2D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b4222-103">Direct2D constants</span></span>

<span data-ttu-id="b4222-104">Die folgenden Konstanten werden in den `d2d1effectauthor.h` `d2d1.h` `d2d1_1.h` Header Dateien,, und deklariert `d2d1effects_2.h` .</span><span class="sxs-lookup"><span data-stu-id="b4222-104">The following constants are declared in the `d2d1effectauthor.h`, `d2d1.h`, `d2d1_1.h`, and `d2d1effects_2.h` header files.</span></span>

## <a name="d2d1_append_aligned_element--1"></a><span data-ttu-id="b4222-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span><span class="sxs-lookup"><span data-stu-id="b4222-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span></span>
<span data-ttu-id="b4222-106">Wird verwendet, wenn Eingabe Layout-Elemente verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="b4222-106">Used when packing input layout elements.</span></span> <span data-ttu-id="b4222-107">Gibt an, dass die Elemente zusammenhängend verpackt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b4222-107">It indicates that the elements must be packed contiguously.</span></span>

## <a name="d2d1_default_flattening_tolerance-025f"></a><span data-ttu-id="b4222-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)</span><span class="sxs-lookup"><span data-stu-id="b4222-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25f)</span></span>
<span data-ttu-id="b4222-109">Die Standardtoleranz für geometrische Vereinfachungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="b4222-109">The default tolerance for geometric flattening operations.</span></span>

## <a name="d2d1_invalid_property_index-uint_max"></a><span data-ttu-id="b4222-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span><span class="sxs-lookup"><span data-stu-id="b4222-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span></span>
<span data-ttu-id="b4222-111">Definiert einen ungültigen Eigenschafts Index.</span><span class="sxs-lookup"><span data-stu-id="b4222-111">Defines an invalid property index.</span></span>

<span data-ttu-id="b4222-112">Diese Konstante wird von [**ID2D1Properties:: getpropertyindex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) zurückgegeben, um anzugeben, dass die angegebene benannte Eigenschaft nicht über einen Index in der Eigenschaften Schnittstelle verfügt.</span><span class="sxs-lookup"><span data-stu-id="b4222-112">This constant is returned from [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) to indicate that the named property that you provided doesn't have an index in the property interface.</span></span>

<span data-ttu-id="b4222-113">Wenn Sie diese Konstante an [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) oder [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32))übergeben, schlägt der-Befehl fehl, und der Ausgabepuffer wird mit Nullen gefüllt.</span><span class="sxs-lookup"><span data-stu-id="b4222-113">If you pass this constant to [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) or [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), then the call fails, and the output buffer is zero-filled.</span></span>

## <a name="d2d1_invalid_tag-ulonglong_max"></a><span data-ttu-id="b4222-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span><span class="sxs-lookup"><span data-stu-id="b4222-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span></span>
<span data-ttu-id="b4222-115">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="b4222-115">Reserved; don't use.</span></span>

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a><span data-ttu-id="b4222-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80,0 f)</span><span class="sxs-lookup"><span data-stu-id="b4222-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)</span></span>
<span data-ttu-id="b4222-117">Die Anzahl der Nits, die von sRGB-oder ScRGB-Farbraum für SZR weiß oder Gleit Komma Werte von 1.0 f verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4222-117">The number of nits that sRGB or scRGB color space uses for SDR white, or floating point values of 1.0f.</span></span> <span data-ttu-id="b4222-118">Dieser Wert ist nur konstant, wenn der Farbraum die von der Szene referenzierte Leuchtkraft verwendet. Dies gilt für den Inhalt mit hohem dynamischen Bereich (HDR).</span><span class="sxs-lookup"><span data-stu-id="b4222-118">This value is constant only when the color space uses scene-referred luminance, which is true for high dynamic range (HDR) content.</span></span> <span data-ttu-id="b4222-119">Wenn für den Farbraum die Anzeige von der Anzeige verwendet wird, sollte die e/a-Ebene von der Anzeige abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="b4222-119">If the color space uses display-referred luminance instead, then the SDR white level should be queried from the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4222-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4222-120">Requirements</span></span>

| <span data-ttu-id="b4222-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4222-121">Requirement</span></span> | <span data-ttu-id="b4222-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b4222-122">Value</span></span> |
|-|-|
| <span data-ttu-id="b4222-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4222-123">Minimum supported client</span></span> | <span data-ttu-id="b4222-124">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b4222-124">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="b4222-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4222-125">Minimum supported server</span></span> | <span data-ttu-id="b4222-126">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b4222-126">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="b4222-127">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="b4222-127">Minimum supported phone</span></span> | <span data-ttu-id="b4222-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps \] , Windows Phone 8,1 \[ Windows Phone Silverlight 8,1-und Windows-Runtime-apps\]</span><span class="sxs-lookup"><span data-stu-id="b4222-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\], Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span> |
| <span data-ttu-id="b4222-129">Header</span><span class="sxs-lookup"><span data-stu-id="b4222-129">Header</span></span> | <span data-ttu-id="b4222-130">d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h</span><span class="sxs-lookup"><span data-stu-id="b4222-130">d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h</span></span> |

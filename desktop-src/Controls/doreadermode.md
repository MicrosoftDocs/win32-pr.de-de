---
title: Doreadermode-Funktion
description: Aktiviert den Lesemodus in einem-Fenster.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Windows-Steuerelemente der doreadermode-Funktion
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479471"
---
# <a name="doreadermode-function"></a><span data-ttu-id="5e6b4-104">Doreadermode-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e6b4-104">DoReaderMode function</span></span>

<span data-ttu-id="5e6b4-105">\[**Doreadermode** ist über Windows XP mit Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="5e6b4-106">Er ist möglicherweise in nachfolgenden Versionen nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5e6b4-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5e6b4-107">Aktiviert den Lesemodus in einem-Fenster.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e6b4-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="5e6b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e6b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e6b4-110">*prmi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e6b4-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6b4-111">Typ: **preadermodeinfo**</span><span class="sxs-lookup"><span data-stu-id="5e6b4-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="5e6b4-112">Ein Zeiger auf eine [**readermodeinfo**](readermodeinfo.md) -Struktur, die Initialisierungs Informationen für den Lesemodus enthält.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e6b4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e6b4-113">Return value</span></span>

<span data-ttu-id="5e6b4-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6b4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e6b4-115">Remarks</span></span>

<span data-ttu-id="5e6b4-116">Der Reader-Modus wird über die unterstützten Geräte per Mausklick aktiviert, in der Regel mit einer dritten Maustaste oder einem Mausrad.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="5e6b4-117">Die nachfolgende Mausbewegung in einem angegebenen Bereich führt einen Bildlauf für den Inhalt des Bereichs aus, anstatt einen Zeiger zu verschieben</span><span class="sxs-lookup"><span data-stu-id="5e6b4-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="5e6b4-118">Außerhalb dieses Bereichs wird der Mauszeiger angezeigt und funktioniert normal.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="5e6b4-119">Mit einem zweiten Klick auf die Schaltfläche oder das Mausrad wird das Gerät im Lesemodus freigegeben.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="5e6b4-120">Diese Funktion ist in keinem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-120">This function is not declared in any public header.</span></span> <span data-ttu-id="5e6b4-121">Um es zu verwenden, müssen Sie über Comctl32.dll als Ordnungszahl 383 darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5e6b4-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e6b4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e6b4-122">Requirements</span></span>



| <span data-ttu-id="5e6b4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e6b4-123">Requirement</span></span> | <span data-ttu-id="5e6b4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5e6b4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6b4-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e6b4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5e6b4-126">Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e6b4-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5e6b4-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e6b4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5e6b4-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e6b4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5e6b4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5e6b4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e6b4-130"><dt>Comctl32.dll (Version 4,72 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="5e6b4-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 






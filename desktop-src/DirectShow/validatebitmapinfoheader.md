---
description: Die validatebitmapinfoheader-Funktion überprüft eine BITMAPINFOHEADER-Struktur auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Validatebitmapinfoheader-Funktion (checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364480"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="11385-103">Validatebitmapinfoheader-Funktion</span><span class="sxs-lookup"><span data-stu-id="11385-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="11385-104">Die- `ValidateBitmapInfoHeader` Funktion überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.</span><span class="sxs-lookup"><span data-stu-id="11385-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="11385-105">Diese Funktion garantiert nicht, dass die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur gültig ist oder dass der Code, der die Struktur verwendet, sicher ist.</span><span class="sxs-lookup"><span data-stu-id="11385-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="11385-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11385-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="11385-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="11385-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11385-108">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="11385-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="11385-109">Zeiger auf die zu validierende [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="11385-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="11385-110">*CBSIZE*</span><span class="sxs-lookup"><span data-stu-id="11385-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="11385-111">Größe des Speicherblocks, der die Struktur enthält (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="11385-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11385-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11385-112">Return value</span></span>

<span data-ttu-id="11385-113">Gibt einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="11385-113">Returns a Boolean value.</span></span> <span data-ttu-id="11385-114">Wenn der Wert **false** ist, ist die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur ungültig.</span><span class="sxs-lookup"><span data-stu-id="11385-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="11385-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11385-115">Remarks</span></span>

<span data-ttu-id="11385-116">Diese Funktion schützt vor den folgenden Fehlern:</span><span class="sxs-lookup"><span data-stu-id="11385-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="11385-117">Arithmetischer Überlauf in der Struktur Größe oder einer ungültigen Struktur Größe.</span><span class="sxs-lookup"><span data-stu-id="11385-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="11385-118">Ungültiger Wert für den **biclrused** -Member.</span><span class="sxs-lookup"><span data-stu-id="11385-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="11385-119">Arithmetischer Überlauf in der Bildgröße (**bisizeimage**).</span><span class="sxs-lookup"><span data-stu-id="11385-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="11385-120">Ungültige Werte für die Bildgröße (**bisizeimage**) für RGB-Formate.</span><span class="sxs-lookup"><span data-stu-id="11385-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="11385-121">Die-Funktion prüft nicht, ob die Struktur ein gültiges Videoformat beschreibt.</span><span class="sxs-lookup"><span data-stu-id="11385-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="11385-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11385-122">Requirements</span></span>



| <span data-ttu-id="11385-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11385-123">Requirement</span></span> | <span data-ttu-id="11385-124">Wert</span><span class="sxs-lookup"><span data-stu-id="11385-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11385-125">Header</span><span class="sxs-lookup"><span data-stu-id="11385-125">Header</span></span><br/> | <dl> <span data-ttu-id="11385-126"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11385-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11385-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11385-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11385-128">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="11385-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





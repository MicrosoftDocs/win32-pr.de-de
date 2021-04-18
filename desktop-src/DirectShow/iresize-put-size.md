---
description: Die Put \_ size-Methode legt die Ausgabegröße und den streckungs Modus fest.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: Iresize::p ut_Size-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368378"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="9166c-103">Iresize::p UT \_ size-Methode</span><span class="sxs-lookup"><span data-stu-id="9166c-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="9166c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9166c-104">\[Deprecated.</span></span> <span data-ttu-id="9166c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9166c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9166c-106">Die `put_Size` -Methode legt die Ausgabegröße und den streckungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="9166c-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="9166c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9166c-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="9166c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9166c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9166c-109">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9166c-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9166c-110">Die Höhe des Videos in Pixel.</span><span class="sxs-lookup"><span data-stu-id="9166c-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9166c-111">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9166c-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9166c-112">Die Breite des Videos in Pixel.</span><span class="sxs-lookup"><span data-stu-id="9166c-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9166c-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9166c-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9166c-114">Der streckungs Modus.</span><span class="sxs-lookup"><span data-stu-id="9166c-114">The stretch mode.</span></span> <span data-ttu-id="9166c-115">Informationen zu möglichen Werten finden Sie unter [**Größenänderung für Flags**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="9166c-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9166c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9166c-116">Return value</span></span>

<span data-ttu-id="9166c-117">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9166c-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9166c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9166c-118">Remarks</span></span>

<span data-ttu-id="9166c-119">DES kann diese Methode vor oder nach dem Aufruf von **Put \_ mediaType** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9166c-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="9166c-120">Wenn des auf diese Methode vor dem Aufruf von **Put \_ mediaType** aufruft, sollte der Filter einen Standardwert für die Bittiefe auswählen und die Größen Werte zum Erstellen eines Ausgabemedien Typs verwenden.</span><span class="sxs-lookup"><span data-stu-id="9166c-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="9166c-121">Wenn des nach dem Aufruf von **Put \_ mediaType** diese Methode aufruft, sollte der Filter seinen aktuellen Ausgabetyp mit den neuen Größen ändern.</span><span class="sxs-lookup"><span data-stu-id="9166c-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="9166c-122">Des kann diese Methode auch nach der Verbindungs Herstellung der Ausgabe-PIN aufruft.</span><span class="sxs-lookup"><span data-stu-id="9166c-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="9166c-123">Ändern Sie in diesem Fall den Ausgabetyp, und verbinden Sie die Ausgabe-PIN erneut mit dem neuen Typ.</span><span class="sxs-lookup"><span data-stu-id="9166c-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="9166c-124">Weitere Informationen finden Sie unter Wiederherstellen einer [Verbindung mit Pins](reconnecting-pins.md) .</span><span class="sxs-lookup"><span data-stu-id="9166c-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="9166c-125">Der *Flags* -Parameter gibt an, wie der Filter den Vorgang zum Ändern der Größe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="9166c-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="9166c-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9166c-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9166c-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9166c-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9166c-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9166c-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9166c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9166c-129">Requirements</span></span>



| <span data-ttu-id="9166c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9166c-130">Requirement</span></span> | <span data-ttu-id="9166c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9166c-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9166c-132">Version</span><span class="sxs-lookup"><span data-stu-id="9166c-132">Version</span></span><br/> | <span data-ttu-id="9166c-133">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9166c-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="9166c-134">Header</span><span class="sxs-lookup"><span data-stu-id="9166c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9166c-135"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9166c-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9166c-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9166c-136">Library</span></span><br/> | <dl> <span data-ttu-id="9166c-137"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9166c-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9166c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9166c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9166c-139">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="9166c-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="9166c-140">**Iresize-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9166c-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 





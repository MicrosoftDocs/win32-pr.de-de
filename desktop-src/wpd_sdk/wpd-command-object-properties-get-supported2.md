---
description: Ruft die Eigenschaften ab, die von einem-Objekt unterstützt werden.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354687"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="d38f9-103">WPD- \_ Befehls \_ Objekt \_ Eigenschaften \_ Get supported- \_ Befehl</span><span class="sxs-lookup"><span data-stu-id="d38f9-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="d38f9-104">Der Befehl " **\_ \_ \_ \_ get \_ supported" (WPD Command Object Properties** ) Ruft die von einem Objekt unterstützten Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="d38f9-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="d38f9-105">Befehls Kategorie</span><span class="sxs-lookup"><span data-stu-id="d38f9-105">Command Category</span></span>

<span data-ttu-id="d38f9-106">**\_ \_ Objekt \_ Eigenschaften der WPD-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="d38f9-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="d38f9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d38f9-107">Parameters</span></span>

<span data-ttu-id="d38f9-108">Der Treiber erwartet den folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="d38f9-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="d38f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d38f9-109">Parameter</span></span>                                         | <span data-ttu-id="d38f9-110">VarType</span><span class="sxs-lookup"><span data-stu-id="d38f9-110">VarType</span></span>        | <span data-ttu-id="d38f9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d38f9-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="d38f9-112">**Objekt-ID der WPD- \_ \_ \_ Eigenschaften \_ \_ Objekte**</span><span class="sxs-lookup"><span data-stu-id="d38f9-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="d38f9-113">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="d38f9-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d38f9-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d38f9-114">Required.</span></span> <span data-ttu-id="d38f9-115">Die ID des-Objekts, das die angeforderten Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d38f9-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="d38f9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d38f9-116">Return Value</span></span>

<span data-ttu-id="d38f9-117">Als Ergebnisse des Treibers werden erwartet:</span><span class="sxs-lookup"><span data-stu-id="d38f9-117">The driver should return the following results.</span></span>



| <span data-ttu-id="d38f9-118">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d38f9-118">Result</span></span>                                                | <span data-ttu-id="d38f9-119">VarType</span><span class="sxs-lookup"><span data-stu-id="d38f9-119">VarType</span></span>         | <span data-ttu-id="d38f9-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d38f9-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38f9-121">**Eigenschaften Schlüssel für WPD- \_ Eigenschafts \_ Objekt \_ Eigenschaften \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d38f9-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="d38f9-122">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d38f9-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="d38f9-123">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d38f9-123">Required.</span></span> <span data-ttu-id="d38f9-124">Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Schnittstelle, die alle unterstützten Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="d38f9-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="d38f9-125">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d38f9-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="d38f9-126">**VT- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d38f9-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="d38f9-127">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d38f9-127">Required.</span></span> <span data-ttu-id="d38f9-128">Ein **HRESULT** -Wert, der den Gesamterfolg oder Misserfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="d38f9-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="d38f9-129">Mögliche Ergebnis Werte sind [Fehlercodes für tragbare Windows-Geräte](error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d38f9-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="d38f9-130">Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** . andernfalls ist es nicht erforderlich, einen anderen Ergebniswert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d38f9-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="d38f9-131">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="d38f9-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="d38f9-132">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d38f9-132">**VT\_UI4**</span></span>     | <span data-ttu-id="d38f9-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d38f9-133">Optional.</span></span> <span data-ttu-id="d38f9-134">Ein Treiber spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d38f9-134">A driver-specific error code.</span></span> <span data-ttu-id="d38f9-135">Dies wird in der Regel nur für Treiber Tests oder für den Treiber, das Gerät und den Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="d38f9-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="d38f9-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d38f9-136">Requirements</span></span>



| <span data-ttu-id="d38f9-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d38f9-137">Requirement</span></span> | <span data-ttu-id="d38f9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="d38f9-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38f9-139">Header</span><span class="sxs-lookup"><span data-stu-id="d38f9-139">Header</span></span><br/> | <dl> <span data-ttu-id="d38f9-140"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38f9-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38f9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d38f9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38f9-142">**Befehle**</span><span class="sxs-lookup"><span data-stu-id="d38f9-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 





---
description: Der Befehl zum \_ Initiieren der Image Erfassung durch den WPD-Befehl initiiert immer noch \_ \_ \_ \_ eine Image Erfassung durch ein Bild Funktions Objekt. Wenn ein neues Objekt erstellt wird, weil ein Bild erstellt wurde, sollte der Treiber das Ereignis Ereignis hinzufügen des WPD- \_ Ereignisses senden \_ \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364550"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="20ae1-104">Befehl zum \_ \_ Initiieren der \_ Image \_ Erfassung \_ für den WPD-Befehl</span><span class="sxs-lookup"><span data-stu-id="20ae1-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="20ae1-105">Der Befehl zum **Initiieren der \_ \_ \_ Image \_ Erfassung \_ durch den WPD-Befehl** initiiert immer noch eine Image Erfassung durch ein Bild Funktions Objekt.</span><span class="sxs-lookup"><span data-stu-id="20ae1-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="20ae1-106">Wenn ein neues Objekt erstellt wird, weil ein Bild erstellt wurde, sollte der Treiber das Ereignis Ereignis **\_ \_ \_ Hinzufügen des WPD-Ereignisses** senden.</span><span class="sxs-lookup"><span data-stu-id="20ae1-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="20ae1-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="20ae1-107">Command category</span></span>

<span data-ttu-id="20ae1-108">**WPD- \_ Kategorie \_ trotzdem \_ Image \_ Erfassung**</span><span class="sxs-lookup"><span data-stu-id="20ae1-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="20ae1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ae1-109">Parameters</span></span>

<span data-ttu-id="20ae1-110">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="20ae1-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="20ae1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ae1-111">Parameter</span></span>                              | <span data-ttu-id="20ae1-112">VarType</span><span class="sxs-lookup"><span data-stu-id="20ae1-112">VarType</span></span>    | <span data-ttu-id="20ae1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20ae1-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ae1-114">Allgemeine WPD- \_ Eigenschaft ( \_ \_ Befehls \_ Ziel)</span><span class="sxs-lookup"><span data-stu-id="20ae1-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="20ae1-115">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="20ae1-115">VT\_LPWSTR</span></span> | <span data-ttu-id="20ae1-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20ae1-116">Required.</span></span> <span data-ttu-id="20ae1-117">Die Objekt-ID des noch Funktions Objekts der Bild Erfassung auf dem Gerät, das das Bild aufnehmen soll. Jedes funktionale Objekt für die Bild Erfassung kann über unterschiedliche Einstellungen verfügen, und es kann auf eine andere Hardware auf einem Gerät (z. b. eine Vorder-oder rückwärts Kamera eines Telefons) verweisen, und dieser Parameter gibt an, welcher Wert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="20ae1-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="20ae1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20ae1-118">Return Value</span></span>

<span data-ttu-id="20ae1-119">Als Ergebnisse des Treibers werden erwartet:</span><span class="sxs-lookup"><span data-stu-id="20ae1-119">The driver should return the following results.</span></span>



| <span data-ttu-id="20ae1-120">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="20ae1-120">Result</span></span>                                         | <span data-ttu-id="20ae1-121">VarType</span><span class="sxs-lookup"><span data-stu-id="20ae1-121">VarType</span></span>   | <span data-ttu-id="20ae1-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20ae1-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ae1-123">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="20ae1-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="20ae1-124">VT- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="20ae1-124">VT\_ERROR</span></span> | <span data-ttu-id="20ae1-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20ae1-125">Required.</span></span> <span data-ttu-id="20ae1-126">Ein **HRESULT** , das den Erfolg oder Fehler beim Ausführen des Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="20ae1-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="20ae1-127">Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="20ae1-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="20ae1-128">Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="20ae1-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="20ae1-129">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="20ae1-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="20ae1-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="20ae1-130">VT\_UI4</span></span>   | <span data-ttu-id="20ae1-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="20ae1-131">Optional.</span></span> <span data-ttu-id="20ae1-132">Ein Treiber spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="20ae1-132">A driver-specific error code.</span></span> <span data-ttu-id="20ae1-133">Dieser Wert wird in der Regel von Geräte Anbietern verwendet, um die Diagnose von Gerätefehlern bei der Verwendung Ihrer Anwendungen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="20ae1-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="20ae1-134">Anwendungen, die universell verwendet werden, würden Sie ignorieren und \_ \_ verwenden stattdessen ausschließlich das allgemeine HRESULT der WPD-Eigenschaft \_ .</span><span class="sxs-lookup"><span data-stu-id="20ae1-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="20ae1-135">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="20ae1-135">Calling Methods</span></span>

<span data-ttu-id="20ae1-136">Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="20ae1-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="20ae1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20ae1-137">Requirements</span></span>



| <span data-ttu-id="20ae1-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20ae1-138">Requirement</span></span> | <span data-ttu-id="20ae1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="20ae1-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ae1-140">Header</span><span class="sxs-lookup"><span data-stu-id="20ae1-140">Header</span></span><br/> | <dl> <span data-ttu-id="20ae1-141"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ae1-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ae1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20ae1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ae1-143">**Befehle**</span><span class="sxs-lookup"><span data-stu-id="20ae1-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 





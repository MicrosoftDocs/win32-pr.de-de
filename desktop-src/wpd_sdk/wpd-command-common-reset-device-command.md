---
description: Der Befehl "der Befehl" der Befehl " \_ \_ Common \_ Reset \_ Device" setzt das Gerät zurück. Dies bedeutet nicht die Neuformatierung. Dies entspricht dem Ausschalten des Geräts.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: WPD_COMMAND_COMMON_RESET_DEVICE Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369296"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="629b1-104">Befehl zum \_ \_ \_ Zurücksetzen des \_ Geräts für WPD-Befehl</span><span class="sxs-lookup"><span data-stu-id="629b1-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="629b1-105">Der Befehl "der Befehl" der Befehl " **\_ \_ Common \_ Reset \_ Device** " setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="629b1-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="629b1-106">Dies bedeutet nicht die Neuformatierung. Dies entspricht dem Ausschalten des Geräts.</span><span class="sxs-lookup"><span data-stu-id="629b1-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="629b1-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="629b1-107">Command category</span></span>

<span data-ttu-id="629b1-108">**Allgemeine WPD- \_ Kategorie \_**</span><span class="sxs-lookup"><span data-stu-id="629b1-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="629b1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="629b1-109">Parameters</span></span>

<span data-ttu-id="629b1-110">Dieser Befehl weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="629b1-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="629b1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="629b1-111">Return Value</span></span>

<span data-ttu-id="629b1-112">Als Ergebnisse des Treibers werden erwartet:</span><span class="sxs-lookup"><span data-stu-id="629b1-112">The driver should return the following results.</span></span>



| <span data-ttu-id="629b1-113">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="629b1-113">Result</span></span>                                         | <span data-ttu-id="629b1-114">VarType</span><span class="sxs-lookup"><span data-stu-id="629b1-114">VarType</span></span>   | <span data-ttu-id="629b1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="629b1-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="629b1-116">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="629b1-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="629b1-117">VT- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="629b1-117">VT\_ERROR</span></span> | <span data-ttu-id="629b1-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="629b1-118">Required.</span></span> <span data-ttu-id="629b1-119">Ein **HRESULT** , das den Erfolg oder Fehler beim Ausführen des Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="629b1-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="629b1-120">Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="629b1-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="629b1-121">Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="629b1-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="629b1-122">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="629b1-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="629b1-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="629b1-123">VT\_UI4</span></span>   | <span data-ttu-id="629b1-124">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="629b1-124">Optional.</span></span> <span data-ttu-id="629b1-125">Ein Treiber spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="629b1-125">A driver-specific error code.</span></span> <span data-ttu-id="629b1-126">Dies wird in der Regel nur für Treiber Tests verwendet, oder wenn der Treiber, das Gerät und der Client verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="629b1-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="629b1-127">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="629b1-127">Calling Methods</span></span>

<span data-ttu-id="629b1-128">Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="629b1-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="629b1-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="629b1-129">Requirements</span></span>



| <span data-ttu-id="629b1-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="629b1-130">Requirement</span></span> | <span data-ttu-id="629b1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="629b1-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="629b1-132">Header</span><span class="sxs-lookup"><span data-stu-id="629b1-132">Header</span></span><br/> | <dl> <span data-ttu-id="629b1-133"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="629b1-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629b1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="629b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629b1-135">**Befehle**</span><span class="sxs-lookup"><span data-stu-id="629b1-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 





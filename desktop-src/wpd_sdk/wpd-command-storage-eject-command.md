---
description: Mit dem Befehl "WPD \_ Command \_ Storage \_ eject" wird ein Speichermedium eingefügt, das per Remote Zugriff vom Computer entfernt werden kann.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: WPD_COMMAND_STORAGE_EJECT Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361604"
---
# <a name="wpd_command_storage_eject-command"></a><span data-ttu-id="dee58-103">Befehl "Speicher für WPD- \_ Befehl" \_ \_</span><span class="sxs-lookup"><span data-stu-id="dee58-103">WPD\_COMMAND\_STORAGE\_EJECT Command</span></span>

<span data-ttu-id="dee58-104">Mit dem Befehl " **WPD \_ Command \_ Storage \_ eject** " wird ein Speichermedium eingefügt, das per Remote Zugriff vom Computer entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dee58-104">The **WPD\_COMMAND\_STORAGE\_EJECT** command ejects a storage medium that can be ejected remotely by the computer.</span></span>

## <a name="command-category"></a><span data-ttu-id="dee58-105">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="dee58-105">Command category</span></span>

<span data-ttu-id="dee58-106">**WPD \_ - \_ kategoriespeicher**</span><span class="sxs-lookup"><span data-stu-id="dee58-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="dee58-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dee58-107">Parameters</span></span>

<span data-ttu-id="dee58-108">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="dee58-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="dee58-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dee58-109">Parameter</span></span>                          | <span data-ttu-id="dee58-110">VarType</span><span class="sxs-lookup"><span data-stu-id="dee58-110">VarType</span></span>    | <span data-ttu-id="dee58-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dee58-111">Description</span></span>                                             |
|------------------------------------|------------|---------------------------------------------------------|
| <span data-ttu-id="dee58-112">WPD- \_ Eigenschaften \_ Speicher Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="dee58-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="dee58-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="dee58-113">VT\_LPWSTR</span></span> | <span data-ttu-id="dee58-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dee58-114">Required.</span></span> <span data-ttu-id="dee58-115">Die Objekt-ID des zu ausgelösten Speicher Objekts.</span><span class="sxs-lookup"><span data-stu-id="dee58-115">The object ID of the storage object to eject.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="dee58-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dee58-116">Return Value</span></span>

<span data-ttu-id="dee58-117">Als Ergebnisse des Treibers werden erwartet:</span><span class="sxs-lookup"><span data-stu-id="dee58-117">The driver should return the following results.</span></span>



| <span data-ttu-id="dee58-118">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="dee58-118">Result</span></span>                                         | <span data-ttu-id="dee58-119">VarType</span><span class="sxs-lookup"><span data-stu-id="dee58-119">VarType</span></span>   | <span data-ttu-id="dee58-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dee58-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee58-121">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dee58-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="dee58-122">VT- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="dee58-122">VT\_ERROR</span></span> | <span data-ttu-id="dee58-123">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dee58-123">Required.</span></span> <span data-ttu-id="dee58-124">Ein **HRESULT** , das den Erfolg oder Fehler beim Ausführen des Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="dee58-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="dee58-125">Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="dee58-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="dee58-126">Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="dee58-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="dee58-127">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="dee58-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="dee58-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="dee58-128">VT\_UI4</span></span>   | <span data-ttu-id="dee58-129">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="dee58-129">Optional.</span></span> <span data-ttu-id="dee58-130">Ein Treiber spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dee58-130">A driver-specific error code.</span></span> <span data-ttu-id="dee58-131">Dies wird in der Regel nur für Treiber Tests verwendet, oder wenn der Treiber, das Gerät und der Client verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="dee58-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="dee58-132">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="dee58-132">Calling Methods</span></span>

<span data-ttu-id="dee58-133">Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dee58-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="dee58-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dee58-134">Requirements</span></span>



| <span data-ttu-id="dee58-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dee58-135">Requirement</span></span> | <span data-ttu-id="dee58-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dee58-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee58-137">Header</span><span class="sxs-lookup"><span data-stu-id="dee58-137">Header</span></span><br/> | <dl> <span data-ttu-id="dee58-138"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee58-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee58-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dee58-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee58-140">**Befehle**</span><span class="sxs-lookup"><span data-stu-id="dee58-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 





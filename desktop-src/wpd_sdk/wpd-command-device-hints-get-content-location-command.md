---
description: Mit dem Befehl "WPD- \_ Befehl \_ Geräte \_ Hinweise \_ get \_ Content Location" werden \_ die Objekt-IDs von Ordnern abgerufen, die ein Objekt eines bestimmten Typs enthalten können.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368289"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="d572c-103">WPD- \_ Befehl \_ Geräte \_ Hinweise \_ get \_ Content Location- \_ Befehl</span><span class="sxs-lookup"><span data-stu-id="d572c-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="d572c-104">Mit dem Befehl " **WPD- \_ Befehl \_ Geräte \_ Hinweise \_ get \_ Content \_ Location" werden** die Objekt-IDs von Ordnern abgerufen, die ein Objekt eines bestimmten Typs enthalten können.</span><span class="sxs-lookup"><span data-stu-id="d572c-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="d572c-105">Dieser Befehl wird für einen Client schneller bereitgestellt, um zu ermitteln, wo bestimmte Objekte von einem Gerät gespeichert werden, als durch eine Brute-Object-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d572c-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="d572c-106">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="d572c-106">Command category</span></span>

<span data-ttu-id="d572c-107">**WPD- \_ Kategorie \_ Geräte \_ Hinweise**</span><span class="sxs-lookup"><span data-stu-id="d572c-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="d572c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d572c-108">Parameters</span></span>

<span data-ttu-id="d572c-109">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="d572c-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="d572c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d572c-110">Parameter</span></span>                                   | <span data-ttu-id="d572c-111">VarType</span><span class="sxs-lookup"><span data-stu-id="d572c-111">VarType</span></span>   | <span data-ttu-id="d572c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d572c-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d572c-113">Inhaltstyp für WPD- \_ Eigenschaften \_ Geräte \_ Hinweise \_ \_</span><span class="sxs-lookup"><span data-stu-id="d572c-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="d572c-114">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="d572c-114">VT\_CLSID</span></span> | <span data-ttu-id="d572c-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d572c-115">Required.</span></span> <span data-ttu-id="d572c-116">Der Objekttyp, für den der Aufrufer den Container finden möchte.</span><span class="sxs-lookup"><span data-stu-id="d572c-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="d572c-117">Um beispielsweise die Ordner auf der obersten Ebene zu suchen, die zum Speichern von Bildern auf einer digitalen Kamera verwendet werden, sendet der Aufrufer das WPD- \_ \_ Inhaltstyp \_ Image.</span><span class="sxs-lookup"><span data-stu-id="d572c-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="d572c-118">Eine Liste der Objekttypen, die von tragbaren Windows-Geräten definiert werden, finden Sie unter [Anforderungen für Objekte](requirements-for-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="d572c-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="d572c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d572c-119">Return Value</span></span>

<span data-ttu-id="d572c-120">Als Ergebnisse des Treibers werden erwartet:</span><span class="sxs-lookup"><span data-stu-id="d572c-120">The driver should return the following results.</span></span>



| <span data-ttu-id="d572c-121">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d572c-121">Result</span></span>                                               | <span data-ttu-id="d572c-122">VarType</span><span class="sxs-lookup"><span data-stu-id="d572c-122">VarType</span></span>     | <span data-ttu-id="d572c-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d572c-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d572c-124">**\_ \_ \_ \_ Inhalts Orte für gerätehinweise \_ für WPD-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="d572c-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="d572c-125">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="d572c-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="d572c-126">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d572c-126">Required.</span></span> <span data-ttu-id="d572c-127">Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) vom Typ VT \_ LPWSTR Values, die die Objekt-IDs von Ordnern angeben, die Objekte des Typs enthalten, der durch den aufrufenden Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d572c-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="d572c-128">Wenn keine Ordner gefunden werden, sollte dies eine leere Liste sein. Die durch das Ergebnis aufgeführten Ordner können Objekte anderer Inhaltstypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d572c-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="d572c-129">Informationen zu Einschränkungen für Ordner finden Sie in der Eigenschaft " [Inhaltstypen für WPD- \_ Ordner \_ \_ \_ zulässig](miscellaneous-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="d572c-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="d572c-130">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d572c-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="d572c-131">VT- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="d572c-131">VT\_ERROR</span></span>   | <span data-ttu-id="d572c-132">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d572c-132">Required.</span></span> <span data-ttu-id="d572c-133">Ein **HRESULT** , das den Erfolg oder das Fehlschlagen der Ausführung des Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="d572c-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="d572c-134">Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d572c-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="d572c-135">Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="d572c-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="d572c-136">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="d572c-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="d572c-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d572c-137">VT\_UI4</span></span>     | <span data-ttu-id="d572c-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d572c-138">Optional.</span></span> <span data-ttu-id="d572c-139">Ein Treiber spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d572c-139">A driver-specific error code.</span></span> <span data-ttu-id="d572c-140">Dies wird in der Regel nur für Treiber Tests verwendet, oder wenn der Treiber, das Gerät und der Client verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d572c-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="d572c-141">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="d572c-141">Calling Methods</span></span>

<span data-ttu-id="d572c-142">Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d572c-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="d572c-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d572c-143">Requirements</span></span>



| <span data-ttu-id="d572c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d572c-144">Requirement</span></span> | <span data-ttu-id="d572c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="d572c-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d572c-146">Header</span><span class="sxs-lookup"><span data-stu-id="d572c-146">Header</span></span><br/> | <dl> <span data-ttu-id="d572c-147"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d572c-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 





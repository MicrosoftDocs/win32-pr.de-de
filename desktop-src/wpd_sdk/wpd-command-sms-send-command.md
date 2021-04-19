---
description: Der SMS-Send-Befehl des WPD- \_ Befehls \_ \_ initiiert das Senden einer SMS-Nachricht (Short Message Service) durch ein SMS-Funktions Objekt.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: WPD_COMMAND_SMS_SEND Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369449"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="a935d-103">Befehl " \_ \_ SMS \_ Senden" in WPD-Befehl</span><span class="sxs-lookup"><span data-stu-id="a935d-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="a935d-104">Der **SMS- \_ \_ \_ Send** -Befehl des WPD-Befehls initiiert das Senden einer SMS-Nachricht (Short Message Service) durch ein SMS-Funktions Objekt.</span><span class="sxs-lookup"><span data-stu-id="a935d-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="a935d-105">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="a935d-105">Command category</span></span>

<span data-ttu-id="a935d-106">**WPD- \_ Kategorie \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="a935d-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="a935d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a935d-107">Parameters</span></span>

<span data-ttu-id="a935d-108">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="a935d-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="a935d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a935d-109">Parameter</span></span>                              | <span data-ttu-id="a935d-110">VarType</span><span class="sxs-lookup"><span data-stu-id="a935d-110">VarType</span></span>             | <span data-ttu-id="a935d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a935d-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a935d-112">Allgemeine WPD- \_ Eigenschaft ( \_ \_ Befehls \_ Ziel)</span><span class="sxs-lookup"><span data-stu-id="a935d-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="a935d-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a935d-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="a935d-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a935d-114">Required.</span></span> <span data-ttu-id="a935d-115">Die Objekt-ID des SMS-Funktions Objekts, das die Nachricht senden soll.</span><span class="sxs-lookup"><span data-stu-id="a935d-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="a935d-116">Verschiedene SMS-funktionale Objekte können unterschiedliche Einstellungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a935d-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="a935d-117">SMS-Empfänger der WPD- \_ Eigenschaft \_ \_</span><span class="sxs-lookup"><span data-stu-id="a935d-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="a935d-118">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a935d-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="a935d-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a935d-119">Required.</span></span> <span data-ttu-id="a935d-120">Der URI des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="a935d-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="a935d-121">SMS- \_ \_ \_ \_ Nachrichtentyp der WPD-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a935d-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="a935d-122">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="a935d-122">VT\_UI4</span></span>             | <span data-ttu-id="a935d-123">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a935d-123">Required.</span></span> <span data-ttu-id="a935d-124">Ein [**SMS- \_ Nachrichten \_ Typen**](sms-message-types.md) Enumerator, der den Typ der Nachricht angibt (Text oder binär).</span><span class="sxs-lookup"><span data-stu-id="a935d-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="a935d-125">SMS- \_ \_ \_ Text \_ Nachricht für WPD-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a935d-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="a935d-126">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a935d-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="a935d-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a935d-127">Optional.</span></span> <span data-ttu-id="a935d-128">Wenn der **\_ SMS- \_ \_ \_ Nachrichtentyp der WPD-Eigenschaft** eine Textnachricht angibt, ist dies die Meldungs Zeichenfolge; andernfalls wird dieser Parameter nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a935d-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="a935d-129">WPD- \_ Eigenschaft, \_ SMS- \_ Binär \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a935d-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="a935d-130">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="a935d-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="a935d-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a935d-131">Optional.</span></span> <span data-ttu-id="a935d-132">Wenn der **\_ SMS- \_ \_ \_ Nachrichtentyp der WPD-Eigenschaft** eine binäre Nachricht angibt, ist dies ein Zeiger auf ein Bytearray. andernfalls ist dieser Parameter nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a935d-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="a935d-133">Das erste DWORD des Werts ist die Länge des Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a935d-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="a935d-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a935d-134">Return Value</span></span>

<span data-ttu-id="a935d-135">Als Ergebnisse des Treibers werden erwartet:</span><span class="sxs-lookup"><span data-stu-id="a935d-135">The driver should return the following results.</span></span>



| <span data-ttu-id="a935d-136">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a935d-136">Result</span></span>                                         | <span data-ttu-id="a935d-137">VarType</span><span class="sxs-lookup"><span data-stu-id="a935d-137">VarType</span></span>   | <span data-ttu-id="a935d-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a935d-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a935d-139">**WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a935d-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="a935d-140">VT- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="a935d-140">VT\_ERROR</span></span> | <span data-ttu-id="a935d-141">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a935d-141">Required.</span></span> <span data-ttu-id="a935d-142">Ein **HRESULT** , das den Erfolg oder Fehler beim Ausführen des Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="a935d-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="a935d-143">Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a935d-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="a935d-144">Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="a935d-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="a935d-145">**WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**</span><span class="sxs-lookup"><span data-stu-id="a935d-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="a935d-146">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="a935d-146">VT\_UI4</span></span>   | <span data-ttu-id="a935d-147">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a935d-147">Optional.</span></span> <span data-ttu-id="a935d-148">Ein Treiber spezifischer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a935d-148">A driver-specific error code.</span></span> <span data-ttu-id="a935d-149">Dies wird in der Regel nur für Treiber Tests verwendet, oder wenn der Treiber, das Gerät und der Client verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a935d-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="a935d-150">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="a935d-150">Calling Methods</span></span>

<span data-ttu-id="a935d-151">Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a935d-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="a935d-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a935d-152">Requirements</span></span>



| <span data-ttu-id="a935d-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a935d-153">Requirement</span></span> | <span data-ttu-id="a935d-154">Wert</span><span class="sxs-lookup"><span data-stu-id="a935d-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a935d-155">Header</span><span class="sxs-lookup"><span data-stu-id="a935d-155">Header</span></span><br/> | <dl> <span data-ttu-id="a935d-156"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a935d-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a935d-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a935d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a935d-158">**Befehle**</span><span class="sxs-lookup"><span data-stu-id="a935d-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 





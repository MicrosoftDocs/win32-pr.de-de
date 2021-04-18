---
description: Mit dem Befehl "MTP ext-Daten lesen" des WPD- \_ Befehls werden \_ \_ \_ \_ Daten vom Gerät abgerufen, nachdem der Befehl " \_ MTP ext ausführen" des Befehls "WPD-Befehl mit dem Befehl \_ \_ \_ \_ \_ \_ \_ zum Lesen von Daten \_
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358661"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a><span data-ttu-id="80ef5-103">WPD- \_ Befehl \_ MTP \_ ext-Befehl zum Lesen von \_ \_ Daten</span><span class="sxs-lookup"><span data-stu-id="80ef5-103">WPD\_COMMAND\_MTP\_EXT\_READ\_DATA Command</span></span>

<span data-ttu-id="80ef5-104">Mit dem Befehl " **\_ \_ MTP \_ Ext \_ \_** -Daten lesen" des WPD-Befehls werden Daten vom Gerät abgerufen, nachdem der Befehl " **\_ \_ MTP \_ Ext \_ Ausführen \_ \_ \_ \_ \_** " des Befehls "WPD-Befehl mit dem Befehl zum Lesen von Daten</span><span class="sxs-lookup"><span data-stu-id="80ef5-104">The **WPD\_COMMAND\_MTP\_EXT\_READ\_DATA** command retrieves data from the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="80ef5-105">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="80ef5-105">Command category</span></span>

<span data-ttu-id="80ef5-106">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="80ef5-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="80ef5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="80ef5-107">Parameters</span></span>

<span data-ttu-id="80ef5-108">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="80ef5-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="80ef5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="80ef5-109">Parameter</span></span>                                                   | <span data-ttu-id="80ef5-110">VarType</span><span class="sxs-lookup"><span data-stu-id="80ef5-110">VarType</span></span>             | <span data-ttu-id="80ef5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80ef5-111">Description</span></span>                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80ef5-112">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="80ef5-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>              | <span data-ttu-id="80ef5-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="80ef5-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="80ef5-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80ef5-114">Required.</span></span> <span data-ttu-id="80ef5-115">Gibt den Kontext an, der durch den vorherigen-Anrufe des Geräts zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="80ef5-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="80ef5-116">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ überträgt \_ NUM \_ Bytes \_ in den \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="80ef5-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_READ**</span></span> | <span data-ttu-id="80ef5-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="80ef5-117">VT\_UI4</span></span>             | <span data-ttu-id="80ef5-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80ef5-118">Required.</span></span> <span data-ttu-id="80ef5-119">Gibt die Anzahl der zu lesenden Bytes an.</span><span class="sxs-lookup"><span data-stu-id="80ef5-119">Specifies the number of bytes to read.</span></span>                                       |
| <span data-ttu-id="80ef5-120">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragungs \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="80ef5-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                 | <span data-ttu-id="80ef5-121">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="80ef5-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="80ef5-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80ef5-122">Required.</span></span> <span data-ttu-id="80ef5-123">Identifiziert den Puffer, in den die Gerätedaten kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="80ef5-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="80ef5-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80ef5-124">Return Value</span></span>

<span data-ttu-id="80ef5-125">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="80ef5-125">The driver returns the following results.</span></span>



| <span data-ttu-id="80ef5-126">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="80ef5-126">Result</span></span>                                                  | <span data-ttu-id="80ef5-127">VarType</span><span class="sxs-lookup"><span data-stu-id="80ef5-127">VarType</span></span>             | <span data-ttu-id="80ef5-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80ef5-128">Description</span></span>                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| <span data-ttu-id="80ef5-129">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragung \_ NUM \_ Bytes \_ gelesen**</span><span class="sxs-lookup"><span data-stu-id="80ef5-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_READ**</span></span> | <span data-ttu-id="80ef5-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="80ef5-130">VT\_UI4</span></span>             | <span data-ttu-id="80ef5-131">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80ef5-131">Required.</span></span> <span data-ttu-id="80ef5-132">Gibt die Anzahl von Bytes an, die vom Gerät empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="80ef5-132">Specifies the number of bytes received from the device.</span></span> |
| <span data-ttu-id="80ef5-133">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragungs \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="80ef5-133">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>             | <span data-ttu-id="80ef5-134">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="80ef5-134">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="80ef5-135">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80ef5-135">Required.</span></span> <span data-ttu-id="80ef5-136">Der Puffer, der die Gerätedaten enthält.</span><span class="sxs-lookup"><span data-stu-id="80ef5-136">The buffer that contains the device data.</span></span>               |



 

## <a name="calling-methods"></a><span data-ttu-id="80ef5-137">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="80ef5-137">Calling Methods</span></span>

<span data-ttu-id="80ef5-138">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="80ef5-138">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="80ef5-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80ef5-139">Requirements</span></span>



| <span data-ttu-id="80ef5-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80ef5-140">Requirement</span></span> | <span data-ttu-id="80ef5-141">Wert</span><span class="sxs-lookup"><span data-stu-id="80ef5-141">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ef5-142">Header</span><span class="sxs-lookup"><span data-stu-id="80ef5-142">Header</span></span><br/> | <dl> <span data-ttu-id="80ef5-143"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="80ef5-143"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80ef5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80ef5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ef5-145">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="80ef5-145">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 





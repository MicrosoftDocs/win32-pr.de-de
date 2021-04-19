---
description: Der Befehl " \_ MTP ext-Schreib Daten schreiben" des WPD-Befehls \_ \_ \_ \_ sendet Daten an das Gerät, nachdem der Befehl " \_ MTP ext ausführen" des Befehls " \_ MTP \_ ext ausführen" \_ mit dem \_ Befehl " \_ \_ Daten \_ \_
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: WPD_COMMAND_MTP_EXT_WRITE_DATA Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368655"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="bc6cd-103">WPD- \_ Befehl \_ MTP \_ ext-Befehl zum Schreiben von \_ \_ Daten</span><span class="sxs-lookup"><span data-stu-id="bc6cd-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="bc6cd-104">Der Befehl " **\_ \_ MTP \_ Ext- \_ Schreib \_ Daten schreiben" des WPD-Befehls** sendet Daten an das Gerät, nachdem der Befehl " **MTP ext ausführen" des Befehls " \_ \_ MTP \_ ext ausführen" \_ \_ \_ mit \_ \_ \_** dem Befehl "Daten</span><span class="sxs-lookup"><span data-stu-id="bc6cd-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="bc6cd-105">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="bc6cd-105">Command category</span></span>

<span data-ttu-id="bc6cd-106">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="bc6cd-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="bc6cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6cd-107">Parameters</span></span>

<span data-ttu-id="bc6cd-108">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="bc6cd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6cd-109">Parameter</span></span>                                                    | <span data-ttu-id="bc6cd-110">VarType</span><span class="sxs-lookup"><span data-stu-id="bc6cd-110">VarType</span></span>             | <span data-ttu-id="bc6cd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc6cd-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6cd-112">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="bc6cd-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="bc6cd-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="bc6cd-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="bc6cd-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-114">Required.</span></span> <span data-ttu-id="bc6cd-115">Gibt den Kontext an, der durch den vorherigen-Anrufe des Geräts zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="bc6cd-116">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ überträgt \_ NUM \_ Bytes \_ zum \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="bc6cd-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="bc6cd-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bc6cd-117">VT\_UI4</span></span>             | <span data-ttu-id="bc6cd-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-118">Required.</span></span> <span data-ttu-id="bc6cd-119">Gibt die Anzahl der zu schreibenden Bytes an.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="bc6cd-120">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragungs \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="bc6cd-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="bc6cd-121">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="bc6cd-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="bc6cd-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-122">Required.</span></span> <span data-ttu-id="bc6cd-123">Identifiziert den Puffer, in den die Gerätedaten kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="bc6cd-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc6cd-124">Return Value</span></span>

<span data-ttu-id="bc6cd-125">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-125">The driver returns the following results.</span></span>



| <span data-ttu-id="bc6cd-126">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="bc6cd-126">Result</span></span>                                                     | <span data-ttu-id="bc6cd-127">VarType</span><span class="sxs-lookup"><span data-stu-id="bc6cd-127">VarType</span></span> | <span data-ttu-id="bc6cd-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc6cd-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="bc6cd-129">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragung \_ NUM \_ Bytes \_ geschrieben**</span><span class="sxs-lookup"><span data-stu-id="bc6cd-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="bc6cd-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bc6cd-130">VT\_UI4</span></span> | <span data-ttu-id="bc6cd-131">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-131">Required.</span></span> <span data-ttu-id="bc6cd-132">Gibt die Anzahl der Bytes an, die an das Gerät gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="bc6cd-133">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="bc6cd-133">Calling Methods</span></span>

<span data-ttu-id="bc6cd-134">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bc6cd-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6cd-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc6cd-135">Requirements</span></span>



| <span data-ttu-id="bc6cd-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc6cd-136">Requirement</span></span> | <span data-ttu-id="bc6cd-137">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6cd-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6cd-138">Header</span><span class="sxs-lookup"><span data-stu-id="bc6cd-138">Header</span></span><br/> | <dl> <span data-ttu-id="bc6cd-139"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc6cd-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc6cd-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc6cd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6cd-141">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="bc6cd-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 





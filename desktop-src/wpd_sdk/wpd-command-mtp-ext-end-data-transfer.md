---
description: Mit dem Befehl "MTP ext" der WPD \_ -Befehl " \_ \_ \_ End \_ Data Transfer" wird \_ eine Datenübertragung und eine Lese Antwort vom Gerät abgeschlossen.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354738"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="83432-103">WPD- \_ Befehl \_ MTP ext Befehl zum Beenden der \_ \_ \_ Daten \_ Übertragung</span><span class="sxs-lookup"><span data-stu-id="83432-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="83432-104">Mit dem Befehl " **MTP ext" der WPD- \_ Befehl " \_ \_ \_ End \_ Data \_ Transfer** " wird eine Datenübertragung und eine Lese Antwort vom Gerät abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="83432-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="83432-105">Die Übertragung wird entweder durch den [**WPD- \_ Befehl \_ MTP \_ Ext \_ Execute \_ Command \_ mit \_ Daten \_ zum \_ Lesen**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) -Befehl oder den [**WPD- \_ Befehl \_ MTP \_ Ext \_ Execute Command mit dem Befehl \_ \_ \_ \_ zum \_ Schreiben von Daten**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) initiiert.</span><span class="sxs-lookup"><span data-stu-id="83432-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="83432-106">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="83432-106">Command category</span></span>

<span data-ttu-id="83432-107">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="83432-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="83432-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83432-108">Parameters</span></span>

<span data-ttu-id="83432-109">Der Treiber erwartet die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="83432-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="83432-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83432-110">Parameter</span></span>                                      | <span data-ttu-id="83432-111">VarType</span><span class="sxs-lookup"><span data-stu-id="83432-111">VarType</span></span>    | <span data-ttu-id="83432-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83432-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="83432-113">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="83432-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="83432-114">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="83432-114">VT\_LPWSTR</span></span> | <span data-ttu-id="83432-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83432-115">Required.</span></span> <span data-ttu-id="83432-116">Identifiziert den Kontext, der von einem früheren Methoden Aufrufwert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83432-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="83432-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83432-117">Return Value</span></span>

<span data-ttu-id="83432-118">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="83432-118">The driver returns the following results.</span></span>



| <span data-ttu-id="83432-119">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="83432-119">Result</span></span>                                        | <span data-ttu-id="83432-120">VarType</span><span class="sxs-lookup"><span data-stu-id="83432-120">VarType</span></span> | <span data-ttu-id="83432-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83432-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83432-122">**WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Antwort \_ Code**</span><span class="sxs-lookup"><span data-stu-id="83432-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="83432-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="83432-123">VT\_UI4</span></span> | <span data-ttu-id="83432-124">Erforderlich. der Antwort Code für den Vorgangs Code des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="83432-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="83432-125">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Antwort \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="83432-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="83432-126">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="83432-126">VT\_UI4</span></span> | <span data-ttu-id="83432-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="83432-127">Optional.</span></span> <span data-ttu-id="83432-128">Eine **iportabledevicepropvariantcollection** -Auflistung, die alle Antwort Parameter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="83432-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="83432-129">Diese Auflistung kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="83432-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="83432-130">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="83432-130">Calling Methods</span></span>

<span data-ttu-id="83432-131">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83432-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="83432-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83432-132">Requirements</span></span>



| <span data-ttu-id="83432-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83432-133">Requirement</span></span> | <span data-ttu-id="83432-134">Wert</span><span class="sxs-lookup"><span data-stu-id="83432-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83432-135">Header</span><span class="sxs-lookup"><span data-stu-id="83432-135">Header</span></span><br/> | <dl> <span data-ttu-id="83432-136"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="83432-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83432-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83432-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83432-138">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="83432-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 


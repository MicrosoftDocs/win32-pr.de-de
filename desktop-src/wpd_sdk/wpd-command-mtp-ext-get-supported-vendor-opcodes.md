---
description: Der WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Supported \_ Vendor \_ Opcodes sendet einen MTP-Befehls Block. Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369168"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="315fd-104">WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Supported \_ Vendor \_ Opcodes Befehl</span><span class="sxs-lookup"><span data-stu-id="315fd-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="315fd-105">Der **WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Supported \_ Vendor \_ Opcodes** sendet einen MTP-Befehls Block.</span><span class="sxs-lookup"><span data-stu-id="315fd-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="315fd-106">Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="315fd-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="315fd-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="315fd-107">Command category</span></span>

<span data-ttu-id="315fd-108">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="315fd-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="315fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="315fd-109">Parameters</span></span>

<span data-ttu-id="315fd-110">Dieser Befehl weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="315fd-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="315fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="315fd-111">Return Value</span></span>

<span data-ttu-id="315fd-112">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="315fd-112">The driver returns the following results.</span></span>



| <span data-ttu-id="315fd-113">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="315fd-113">Result</span></span>                                                | <span data-ttu-id="315fd-114">VarType</span><span class="sxs-lookup"><span data-stu-id="315fd-114">VarType</span></span> | <span data-ttu-id="315fd-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="315fd-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="315fd-116">**WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Hersteller \_ Vorgangs \_ Codes**</span><span class="sxs-lookup"><span data-stu-id="315fd-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="315fd-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="315fd-117">VT\_UI4</span></span> | <span data-ttu-id="315fd-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="315fd-118">Required.</span></span> <span data-ttu-id="315fd-119">Eine **iportabledevicepropvariantcollection** , die alle vom Hersteller erweiterten Vorgangs Codes enthält.</span><span class="sxs-lookup"><span data-stu-id="315fd-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="315fd-120">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="315fd-120">Calling Methods</span></span>

<span data-ttu-id="315fd-121">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="315fd-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="315fd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="315fd-122">Requirements</span></span>



| <span data-ttu-id="315fd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="315fd-123">Requirement</span></span> | <span data-ttu-id="315fd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="315fd-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="315fd-125">Header</span><span class="sxs-lookup"><span data-stu-id="315fd-125">Header</span></span><br/> | <dl> <span data-ttu-id="315fd-126"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315fd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="315fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315fd-128">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="315fd-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 





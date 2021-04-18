---
description: Der Befehl WPD \_ \_ -Befehl MTP \_ Ext \_ get \_ Vendor \_ Extension \_ Description Ruft die Beschreibungs Zeichenfolge der Hersteller Erweiterung ab. Diese Zeichenfolge wird durch ein "Debug"-DataSet definiert.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365695"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="47dd8-104">WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Vendor \_ Extension Description- \_ Befehl</span><span class="sxs-lookup"><span data-stu-id="47dd8-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="47dd8-105">Der Befehl **WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Vendor \_ Extension \_ Description** Ruft die Beschreibungs Zeichenfolge der Hersteller Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="47dd8-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="47dd8-106">Diese **Zeichenfolge wird durch ein "** Debug"-DataSet definiert.</span><span class="sxs-lookup"><span data-stu-id="47dd8-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="47dd8-107">Befehlskategorie</span><span class="sxs-lookup"><span data-stu-id="47dd8-107">Command category</span></span>

<span data-ttu-id="47dd8-108">**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="47dd8-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="47dd8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47dd8-109">Parameters</span></span>

<span data-ttu-id="47dd8-110">Dieser Befehl weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="47dd8-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47dd8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47dd8-111">Return Value</span></span>

<span data-ttu-id="47dd8-112">Der Treiber gibt die folgenden Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="47dd8-112">The driver returns the following results.</span></span>



| <span data-ttu-id="47dd8-113">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="47dd8-113">Result</span></span>                                                      | <span data-ttu-id="47dd8-114">VarType</span><span class="sxs-lookup"><span data-stu-id="47dd8-114">VarType</span></span>    | <span data-ttu-id="47dd8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47dd8-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="47dd8-116">**WPD- \_ Eigenschaft \_ MTP \_ Ext \_ Hersteller \_ Erweiterung \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47dd8-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="47dd8-117">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="47dd8-117">VT\_LPWSTR</span></span> | <span data-ttu-id="47dd8-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47dd8-118">Required.</span></span> <span data-ttu-id="47dd8-119">Gibt die Beschreibungs Zeichenfolge der Hersteller Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="47dd8-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="47dd8-120">Aufrufen von Methoden</span><span class="sxs-lookup"><span data-stu-id="47dd8-120">Calling Methods</span></span>

<span data-ttu-id="47dd8-121">Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47dd8-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="47dd8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47dd8-122">Requirements</span></span>



| <span data-ttu-id="47dd8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47dd8-123">Requirement</span></span> | <span data-ttu-id="47dd8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="47dd8-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="47dd8-125">Header</span><span class="sxs-lookup"><span data-stu-id="47dd8-125">Header</span></span><br/> | <dl> <span data-ttu-id="47dd8-126"><dt>Wpdmtpextensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="47dd8-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47dd8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47dd8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47dd8-128">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="47dd8-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 





---
description: 'IWiaDevMgr2::SelectDeviceDlgID-Methode: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.'
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: IWiaDevMgr2::SelectDeviceDlgID-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106818"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="6a816-103">IWiaDevMgr2::SelectDeviceDlgID-Methode</span><span class="sxs-lookup"><span data-stu-id="6a816-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="6a816-104">Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="6a816-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a816-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a816-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="6a816-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a816-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a816-107">*hwndParent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a816-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a816-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="6a816-108">Type: **HWND**</span></span>

<span data-ttu-id="6a816-109">Gibt das übergeordnete Fenster des Dialogfelds **Gerät auswählen** an.</span><span class="sxs-lookup"><span data-stu-id="6a816-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="6a816-110">*lDeviceType* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a816-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a816-111">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="6a816-111">Type: **LONG**</span></span>

<span data-ttu-id="6a816-112">Gibt an, welcher WIA 2.0-Gerätetyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a816-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="6a816-113">Eine Liste der möglichen Werte finden Sie unter [WIA-Gerätetypspezifizierer.](-wia-wia-device-type-specifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6a816-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="6a816-114">*lFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a816-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a816-115">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="6a816-115">Type: **LONG**</span></span>

<span data-ttu-id="6a816-116">Gibt das Verhalten des Dialogfelds an.</span><span class="sxs-lookup"><span data-stu-id="6a816-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="6a816-117">Der Wert kann einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="6a816-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="6a816-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="6a816-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="6a816-119">Verwendet das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="6a816-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="6a816-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="6a816-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="6a816-121">Zeigt das Dialogfeld an, obwohl nur ein übereinstimmendes Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6a816-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6a816-122">*pbstrDeviceID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6a816-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6a816-123">Typ: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="6a816-123">Type: **BSTR\***</span></span>

<span data-ttu-id="6a816-124">Zeiger auf eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts empfängt.</span><span class="sxs-lookup"><span data-stu-id="6a816-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a816-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a816-125">Return value</span></span>

<span data-ttu-id="6a816-126">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a816-126">Type: **HRESULT**</span></span>

<span data-ttu-id="6a816-127">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6a816-127">This method can return one of these values.</span></span>



| <span data-ttu-id="6a816-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6a816-128">Return code</span></span>                                                                                                  | <span data-ttu-id="6a816-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a816-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a816-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6a816-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="6a816-131">Das Gerät wurde erfolgreich ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6a816-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="6a816-132"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="6a816-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="6a816-133">Der Benutzer hat das Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6a816-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="6a816-134"><dt>**WIA \_ S KEIN GERÄT \_ \_ \_ VERFÜGBAR**</dt></span><span class="sxs-lookup"><span data-stu-id="6a816-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="6a816-135">Keine WIA 2.0-Hardwaregeräte entsprechen den Im *lDeviceType-Parameter angegebenen* Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6a816-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a816-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a816-136">Remarks</span></span>

<span data-ttu-id="6a816-137">Diese Methode erstellt und zeigt das **Dialogfeld Gerät** auswählen an, damit der Benutzer ein WIA 2.0-Gerät für die Bilderfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="6a816-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="6a816-138">Wenn ein Gerät erfolgreich ausgewählt wurde, übergibt die **IWiaDevMgr2::SelectDeviceDlgID-Methode** seine Bezeichnerzeichenfolge über den *parameter pbstrDeviceID* an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6a816-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="6a816-139">Die Anwendung kann die dem Benutzer angezeigten Geräte auf bestimmte Typen beschränken, indem sie die Gerätetypen über den *Parameter lDeviceType* angibt.</span><span class="sxs-lookup"><span data-stu-id="6a816-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="6a816-140">Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2::SelectDeviceDlgID** das Dialogfeld **Gerät** auswählen nicht an.</span><span class="sxs-lookup"><span data-stu-id="6a816-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="6a816-141">Stattdessen wird die Bezeichnerzeichenfolge des Geräts an die Anwendung übergeben, ohne das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a816-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="6a816-142">Sie können dieses Verhalten außer Kraft setzen und **IWiaDevMgr2::SelectDeviceDlgID** zwingen, das Dialogfeld anzuzeigen, indem Sie WIA SELECT DEVICE NODEFAULT als Wert für den \_ \_ \_ *lFlags-Parameter* übergeben.</span><span class="sxs-lookup"><span data-stu-id="6a816-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="6a816-143">Wenn mehr als ein WIA 2.0-Gerät der Spezifikation entspricht, werden alle übereinstimmenden Geräte im Dialogfeld AuswählenGeräte angezeigt, damit der Benutzer eines auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="6a816-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="6a816-144">Es wird empfohlen, dass Anwendungen die Geräte- und Bildauswahl über ein Menüelement namens **From scanner** im Menü **Datei verfügbar** machen.</span><span class="sxs-lookup"><span data-stu-id="6a816-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a816-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a816-145">Requirements</span></span>



| <span data-ttu-id="6a816-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a816-146">Requirement</span></span> | <span data-ttu-id="6a816-147">Wert</span><span class="sxs-lookup"><span data-stu-id="6a816-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a816-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a816-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6a816-149">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a816-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a816-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a816-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6a816-151">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a816-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a816-152">Header</span><span class="sxs-lookup"><span data-stu-id="6a816-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a816-153"><dt>Wia.h</dt></span><span class="sxs-lookup"><span data-stu-id="6a816-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a816-154">Idl</span><span class="sxs-lookup"><span data-stu-id="6a816-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a816-155"><dt>Wia.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a816-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 





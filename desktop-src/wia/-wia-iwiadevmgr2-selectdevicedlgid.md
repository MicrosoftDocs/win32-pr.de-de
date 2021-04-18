---
description: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2:: selectdevicedlgid-Methode (WIA. h)'
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
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347234"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="43610-103">IWiaDevMgr2:: selectdevicedlgid-Methode</span><span class="sxs-lookup"><span data-stu-id="43610-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="43610-104">Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="43610-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="43610-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43610-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="43610-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43610-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43610-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43610-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43610-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="43610-108">Type: **HWND**</span></span>

<span data-ttu-id="43610-109">Gibt das übergeordnete Fenster des Dialog Felds **Gerät auswählen** an.</span><span class="sxs-lookup"><span data-stu-id="43610-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="43610-110">*LDE vicetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43610-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43610-111">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="43610-111">Type: **LONG**</span></span>

<span data-ttu-id="43610-112">Gibt an, welcher Typ von WIA 2,0-Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43610-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="43610-113">Eine Liste der möglichen Werte finden Sie unter [WIA Device Type specifier](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="43610-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="43610-114">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43610-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43610-115">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="43610-115">Type: **LONG**</span></span>

<span data-ttu-id="43610-116">Gibt das Verhalten des Dialog Felds an.</span><span class="sxs-lookup"><span data-stu-id="43610-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="43610-117">Der Wert kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="43610-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="43610-118"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="43610-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="43610-119">Verwendet das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="43610-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="43610-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ Select \_ Device \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="43610-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="43610-121">Zeigt das Dialogfeld an, obwohl nur ein entsprechendes Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="43610-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="43610-122">*pbstraude viceid* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="43610-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="43610-123">Geben Sie Folgendes ein: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="43610-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="43610-124">Zeiger auf eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts empfängt.</span><span class="sxs-lookup"><span data-stu-id="43610-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43610-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43610-125">Return value</span></span>

<span data-ttu-id="43610-126">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="43610-126">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="43610-127">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="43610-127">This method can return one of these values.</span></span>



| <span data-ttu-id="43610-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="43610-128">Return code</span></span>                                                                                                  | <span data-ttu-id="43610-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43610-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43610-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43610-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="43610-131">Das Gerät wurde erfolgreich ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="43610-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="43610-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="43610-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="43610-133">Der Benutzer hat das Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="43610-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="43610-134"><dt>**WIA \_ S \_ kein \_ Gerät \_ verfügbar**</dt></span><span class="sxs-lookup"><span data-stu-id="43610-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="43610-135">Keine WIA 2,0-Hardware Geräte entsprechen den Spezifikationen im *ldebug Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="43610-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="43610-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43610-136">Remarks</span></span>

<span data-ttu-id="43610-137">Mit dieser Methode wird das Dialogfeld **Gerät auswählen** erstellt und angezeigt, sodass der Benutzer ein WIA 2,0-Gerät für die Abbild Erfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="43610-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="43610-138">Wenn ein Gerät erfolgreich ausgewählt wurde, übergibt die **IWiaDevMgr2:: selectdevicedlgid** -Methode die Bezeichnerzeichenfolge über den *pbstraudeviceid* -Parameter an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="43610-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="43610-139">Die Anwendung kann die Geräte, die dem Benutzer angezeigt werden, auf bestimmte Typen beschränken, indem Sie die Gerätetypen über den *ltovicetype* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="43610-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="43610-140">Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2:: selectde vicedlgid** das Dialogfeld **Gerät auswählen** nicht an.</span><span class="sxs-lookup"><span data-stu-id="43610-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="43610-141">Stattdessen wird die Bezeichnerzeichenfolge des Geräts an die Anwendung weitergeleitet, ohne dass das Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="43610-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="43610-142">Sie können dieses Verhalten überschreiben und **IWiaDevMgr2:: selectdevicedlgid** erzwingen, um das Dialogfeld anzuzeigen, indem Sie WIA \_ Select \_ Device \_ NODEFAULT als Wert für den *lFlags* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="43610-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="43610-143">Wenn mehr als ein WIA 2,0-Gerät mit der Spezifikation übereinstimmt, werden alle übereinstimmenden Geräte im Dialogfeld selectdevice angezeigt, sodass der Benutzer eine Auswahl treffen kann.</span><span class="sxs-lookup"><span data-stu-id="43610-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="43610-144">Es wird empfohlen, dass Anwendungen die Geräte-und Abbild Auswahl über ein Menü Element namens **von Scanner** im Menü **Datei** verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="43610-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43610-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43610-145">Requirements</span></span>



| <span data-ttu-id="43610-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43610-146">Requirement</span></span> | <span data-ttu-id="43610-147">Wert</span><span class="sxs-lookup"><span data-stu-id="43610-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43610-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43610-148">Minimum supported client</span></span><br/> | <span data-ttu-id="43610-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43610-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43610-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43610-150">Minimum supported server</span></span><br/> | <span data-ttu-id="43610-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43610-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43610-152">Header</span><span class="sxs-lookup"><span data-stu-id="43610-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="43610-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="43610-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="43610-154">IDL</span><span class="sxs-lookup"><span data-stu-id="43610-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43610-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43610-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 





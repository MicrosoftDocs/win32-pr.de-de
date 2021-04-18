---
description: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2:: SelectDeviceDlg-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358465"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="e36ce-103">IWiaDevMgr2:: SelectDeviceDlg-Methode</span><span class="sxs-lookup"><span data-stu-id="e36ce-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="e36ce-104">Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="e36ce-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e36ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e36ce-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="e36ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e36ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e36ce-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="e36ce-108">Type: **HWND**</span></span>

<span data-ttu-id="e36ce-109">Gibt das übergeordnete Fenster des Dialog Felds **Gerät auswählen** an.</span><span class="sxs-lookup"><span data-stu-id="e36ce-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-110">*LDE vicetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-111">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="e36ce-111">Type: **LONG**</span></span>

<span data-ttu-id="e36ce-112">Gibt an, welcher Typ von WIA 2,0-Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e36ce-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="e36ce-113">Eine Liste der möglichen Werte finden Sie unter [WIA Device Type specifier](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="e36ce-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-114">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-115">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="e36ce-115">Type: **LONG**</span></span>

<span data-ttu-id="e36ce-116">Gibt das Verhalten des Dialog Felds an.</span><span class="sxs-lookup"><span data-stu-id="e36ce-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="e36ce-117">Der Wert kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="e36ce-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e36ce-118"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="e36ce-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="e36ce-119">Verwendet das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="e36ce-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="e36ce-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ Select \_ Device \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e36ce-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="e36ce-121">Zeigt das Dialogfeld an, obwohl nur ein entsprechendes Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e36ce-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e36ce-122">*pbstraude viceid* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-123">Geben Sie Folgendes ein: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="e36ce-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="e36ce-124">Bei der Ausgabe empfängt eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="e36ce-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="e36ce-125">Übergeben Sie bei der Eingabe die Adresse eines Zeigers, wenn diese Informationen benötigt werden, oder _ \*null\*\*, wenn er nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e36ce-125">On input, pass the address of a pointer if this information is needed, or _ *NULL*\* if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-126">*ppitemroot* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-127">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e36ce-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="e36ce-128">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements der hierarchischen Struktur, die das ausgewählte WIA 2,0-Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="e36ce-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="e36ce-129">Wenn kein Gerät gefunden wird, wird **null** empfangen.</span><span class="sxs-lookup"><span data-stu-id="e36ce-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e36ce-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e36ce-130">Return value</span></span>

<span data-ttu-id="e36ce-131">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e36ce-131">Type: **HRESULT**</span></span>

<span data-ttu-id="e36ce-132">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e36ce-132">This method can return one of these values.</span></span>



| <span data-ttu-id="e36ce-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e36ce-133">Return code</span></span>                                                                                                  | <span data-ttu-id="e36ce-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e36ce-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e36ce-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e36ce-136">Das Gerät wurde erfolgreich ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e36ce-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="e36ce-137"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="e36ce-138">Der Benutzer hat das Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e36ce-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="e36ce-139"><dt>**WIA \_ S \_ kein \_ Gerät \_ verfügbar**</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="e36ce-140">Keine WIA 2,0-Hardware Geräte entsprechen den Spezifikationen im *ldebug Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="e36ce-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e36ce-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e36ce-141">Remarks</span></span>

<span data-ttu-id="e36ce-142">Mit dieser Methode wird das Dialogfeld **Gerät auswählen** erstellt und angezeigt, sodass der Benutzer ein WIA 2,0-Gerät für die Abbild Erfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="e36ce-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="e36ce-143">Wenn ein Gerät erfolgreich ausgewählt wurde, erstellt die **IWiaDevMgr2:: SelectDeviceDlg** -Methode eine hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="e36ce-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="e36ce-144">Es speichert einen Zeiger auf die **IWiaItem2** -Schnittstelle des Stamm Elements im Parameter *ppitemroot*.</span><span class="sxs-lookup"><span data-stu-id="e36ce-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="e36ce-145">Die Anwendung kann die Geräte, die dem Benutzer angezeigt werden, auf bestimmte Typen beschränken, indem Sie die Gerätetypen über den *ltovicetype* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="e36ce-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="e36ce-146">Wenn nur ein Gerät der Spezifikation entspricht, wird von **IWiaDevMgr2:: selectde vicedlg** das Dialogfeld **Gerät auswählen** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e36ce-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="e36ce-147">Stattdessen wird die [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur für das Gerät erstellt und ein Zeiger auf die **IWiaItem2** -Schnittstelle des Stamm Elements im Parameter *ppitemroot* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e36ce-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="e36ce-148">Sie können dieses Verhalten überschreiben und **IWiaDevMgr2:: SelectDeviceDlg** erzwingen, um das Dialogfeld anzuzeigen, indem Sie WIA \_ Select \_ Device \_ NODEFAULT als Wert für den *lFlags* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="e36ce-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="e36ce-149">Wenn mehr als ein WIA 2,0-Gerät mit der Spezifikation übereinstimmt, werden alle übereinstimmenden Geräte im Dialogfeld **Gerät auswählen** angezeigt, sodass der Benutzer eine Auswahl treffen kann.</span><span class="sxs-lookup"><span data-stu-id="e36ce-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="e36ce-150">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppitemroot* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="e36ce-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="e36ce-151">Es wird empfohlen, dass Anwendungen die Geräte-und Abbild Auswahl über ein Menü Element namens **von Scanner** im Menü **Datei** verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e36ce-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e36ce-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e36ce-152">Requirements</span></span>



| <span data-ttu-id="e36ce-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e36ce-153">Requirement</span></span> | <span data-ttu-id="e36ce-154">Wert</span><span class="sxs-lookup"><span data-stu-id="e36ce-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e36ce-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e36ce-155">Minimum supported client</span></span><br/> | <span data-ttu-id="e36ce-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e36ce-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e36ce-157">Minimum supported server</span></span><br/> | <span data-ttu-id="e36ce-158">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e36ce-159">Header</span><span class="sxs-lookup"><span data-stu-id="e36ce-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="e36ce-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e36ce-161">IDL</span><span class="sxs-lookup"><span data-stu-id="e36ce-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e36ce-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 

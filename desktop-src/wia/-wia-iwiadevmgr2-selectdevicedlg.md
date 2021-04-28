---
description: 'IWiaDevMgr2::SelectDeviceDlg-Methode: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: IWiaDevMgr2::SelectDeviceDlg-Methode (Wia.h)
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
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091258"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="17ee1-103">IWiaDevMgr2::SelectDeviceDlg-Methode</span><span class="sxs-lookup"><span data-stu-id="17ee1-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="17ee1-104">Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="17ee1-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ee1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17ee1-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="17ee1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17ee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ee1-107">*hwndParent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ee1-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="17ee1-108">Type: **HWND**</span></span>

<span data-ttu-id="17ee1-109">Gibt das übergeordnete Fenster des Dialogfelds **Gerät auswählen** an.</span><span class="sxs-lookup"><span data-stu-id="17ee1-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="17ee1-110">*lDeviceType* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ee1-111">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="17ee1-111">Type: **LONG**</span></span>

<span data-ttu-id="17ee1-112">Gibt an, welcher WiA 2.0-Gerätetyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17ee1-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="17ee1-113">Eine Liste der möglichen Werte finden Sie unter [WIA-Gerätetypspezifizierer.](-wia-wia-device-type-specifiers.md)</span><span class="sxs-lookup"><span data-stu-id="17ee1-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="17ee1-114">*lFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ee1-115">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="17ee1-115">Type: **LONG**</span></span>

<span data-ttu-id="17ee1-116">Gibt das Verhalten des Dialogfelds an.</span><span class="sxs-lookup"><span data-stu-id="17ee1-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="17ee1-117">Der Wert kann einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="17ee1-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="17ee1-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="17ee1-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="17ee1-119">Verwendet das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="17ee1-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="17ee1-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="17ee1-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="17ee1-121">Zeigt das Dialogfeld an, obwohl nur ein übereinstimmendes Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="17ee1-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="17ee1-122">*pbstrDeviceID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17ee1-123">Typ: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="17ee1-123">Type: **BSTR\***</span></span>

<span data-ttu-id="17ee1-124">Empfängt bei der Ausgabe eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="17ee1-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="17ee1-125">Übergeben Sie bei der Eingabe die Adresse eines Zeigers, wenn diese Informationen benötigt werden, oder **NULL,** wenn sie nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="17ee1-125">On input, pass the address of a pointer if this information is needed, or **NULL** if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="17ee1-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="17ee1-127">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="17ee1-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="17ee1-128">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des Stammelements der hierarchischen Struktur, das das ausgewählte WIA 2.0-Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="17ee1-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="17ee1-129">Wenn kein Gerät gefunden wird, empfängt es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="17ee1-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ee1-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17ee1-130">Return value</span></span>

<span data-ttu-id="17ee1-131">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="17ee1-131">Type: **HRESULT**</span></span>

<span data-ttu-id="17ee1-132">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="17ee1-132">This method can return one of these values.</span></span>



| <span data-ttu-id="17ee1-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="17ee1-133">Return code</span></span>                                                                                                  | <span data-ttu-id="17ee1-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17ee1-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17ee1-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17ee1-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="17ee1-136">Das Gerät wurde erfolgreich ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="17ee1-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="17ee1-137"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="17ee1-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="17ee1-138">Der Benutzer hat das Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="17ee1-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="17ee1-139"><dt>**WIA \_ S KEIN GERÄT \_ \_ \_ VERFÜGBAR**</dt></span><span class="sxs-lookup"><span data-stu-id="17ee1-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="17ee1-140">Keine WIA 2.0-Hardwaregeräte entsprechen den Im *lDeviceType-Parameter angegebenen* Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="17ee1-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="17ee1-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17ee1-141">Remarks</span></span>

<span data-ttu-id="17ee1-142">Diese Methode erstellt und zeigt das **Dialogfeld Gerät** auswählen an, damit der Benutzer ein WIA 2.0-Gerät für die Bilderfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="17ee1-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="17ee1-143">Wenn ein Gerät erfolgreich ausgewählt wurde, erstellt die **IWiaDevMgr2::SelectDeviceDlg-Methode** eine hierarchische Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="17ee1-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="17ee1-144">Er speichert einen Zeiger auf die **IWiaItem2-Schnittstelle** des Stammelements im *Parameter ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="17ee1-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="17ee1-145">Die Anwendung kann die dem Benutzer angezeigten Geräte auf bestimmte Typen beschränken, indem sie die Gerätetypen über den *Parameter lDeviceType* angibt.</span><span class="sxs-lookup"><span data-stu-id="17ee1-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="17ee1-146">Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2::SelectDeviceDlg** das Dialogfeld **Gerät** auswählen nicht an.</span><span class="sxs-lookup"><span data-stu-id="17ee1-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="17ee1-147">Stattdessen wird die [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) für das Gerät erstellt und ein Zeiger auf die **IWiaItem2-Schnittstelle** des Stammelements im Parameter *ppItemRoot gespeichert.*</span><span class="sxs-lookup"><span data-stu-id="17ee1-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="17ee1-148">Sie können dieses Verhalten überschreiben und **IWiaDevMgr2::SelectDeviceDlg** zwingen, das Dialogfeld anzuzeigen, indem Sie WIA SELECT DEVICE NODEFAULT als Wert für den \_ \_ \_ *lFlags-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="17ee1-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="17ee1-149">Wenn mehr als ein WIA 2.0-Gerät mit der Spezifikation übereinstimmt, werden alle übereinstimmenden Geräte im Dialogfeld **Gerät auswählen** angezeigt, damit der Benutzer eines auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="17ee1-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="17ee1-150">Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Schnittstellenzeiger aufrufen, die sie über den *ppItemRoot-Parameter* empfangen.</span><span class="sxs-lookup"><span data-stu-id="17ee1-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="17ee1-151">Es wird empfohlen, dass Anwendungen die Geräte- und Bildauswahl über ein Menüelement mit dem Namen **Von Scanner** im Menü **Datei** verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="17ee1-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17ee1-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17ee1-152">Requirements</span></span>



| <span data-ttu-id="17ee1-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17ee1-153">Requirement</span></span> | <span data-ttu-id="17ee1-154">Wert</span><span class="sxs-lookup"><span data-stu-id="17ee1-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17ee1-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17ee1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="17ee1-156">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="17ee1-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17ee1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="17ee1-158">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17ee1-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17ee1-159">Header</span><span class="sxs-lookup"><span data-stu-id="17ee1-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="17ee1-160"><dt>Wia.h</dt></span><span class="sxs-lookup"><span data-stu-id="17ee1-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="17ee1-161">Idl</span><span class="sxs-lookup"><span data-stu-id="17ee1-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17ee1-162"><dt>Wia.idl</dt></span><span class="sxs-lookup"><span data-stu-id="17ee1-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 

---
description: Zeigt dem Benutzer ein Dialogfeld an, in dem die Bild Erfassung vorbereitet werden soll.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2::D evicedlg-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129429"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="bab0d-103">IWiaItem2::D evicedlg-Methode</span><span class="sxs-lookup"><span data-stu-id="bab0d-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="bab0d-104">Zeigt dem Benutzer ein Dialogfeld an, in dem die Bild Erfassung vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bab0d-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab0d-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="bab0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bab0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab0d-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="bab0d-108">Type: **LONG**</span></span>

<span data-ttu-id="bab0d-109">Gibt einen Satz von Flags an, die den Vorgang des Dialog Felds steuern.</span><span class="sxs-lookup"><span data-stu-id="bab0d-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="bab0d-110">Der Wert kann entweder 0 (null) sein, um das Standardverhalten darzustellen, oder eines der WIA- \_ Geräte \_ Dialogfelder, die in [**wiaflag**](-wia-wiaflag.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bab0d-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab0d-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-112">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="bab0d-112">Type: **HWND**</span></span>

<span data-ttu-id="bab0d-113">Ein Handle für das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="bab0d-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="bab0d-114">*bstrinfoldername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-115">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bab0d-115">Type: **BSTR**</span></span>

<span data-ttu-id="bab0d-116">Gibt den Namen des Ordners an, in den die Dateien übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bab0d-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="bab0d-117">*bstrauch filename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-118">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bab0d-118">Type: **BSTR**</span></span>

<span data-ttu-id="bab0d-119">Gibt den Namen der Vorlagen Datei an.</span><span class="sxs-lookup"><span data-stu-id="bab0d-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="bab0d-120">*plnumfiles* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-121">Type: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="bab0d-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="bab0d-122">Ein Zeiger auf die Anzahl der Elemente im _ppbstrFilePaths \*-Array.</span><span class="sxs-lookup"><span data-stu-id="bab0d-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="bab0d-123">*ppbstraufilepfade* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-124">Typ: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="bab0d-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="bab0d-125">Die Adresse eines Zeigers auf ein Array von Pfaden für die gescannten Dateien.</span><span class="sxs-lookup"><span data-stu-id="bab0d-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="bab0d-126">Initialisieren Sie den Zeiger, um auf ein Array der Größe 0 (null) vor IWiaItem2 zu zeigen **::D evicedlg** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bab0d-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="bab0d-127">*ppIWiaItem2* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab0d-128">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bab0d-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="bab0d-129">Die Adresse eines Arrays von Zeigern auf [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="bab0d-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab0d-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bab0d-130">Return value</span></span>

<span data-ttu-id="bab0d-131">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bab0d-131">Type: **HRESULT**</span></span>

<span data-ttu-id="bab0d-132">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bab0d-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bab0d-133">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bab0d-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab0d-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bab0d-134">Remarks</span></span>

<span data-ttu-id="bab0d-135">Diese Methode zeigt dem Benutzer ein Dialogfeld an, das von einer Anwendung verwendet wird, um alle für die Image Erfassung erforderlichen Informationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="bab0d-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="bab0d-136">Sie wird auch verwendet, um Bild Scan Eigenschaften anzugeben, z. b. Helligkeit und Kontrast.</span><span class="sxs-lookup"><span data-stu-id="bab0d-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="bab0d-137">Nachdem diese Methode zurückgegeben wurde, kann die Anwendung die [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle verwenden, um das Image abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bab0d-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="bab0d-138">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für jedes Element im Array von Schnittstellen Zeigern aufrufen, die über den *ppIWiaItem2* -Parameter empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="bab0d-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="bab0d-139">Anwendungen müssen das Array auch mit " [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)" freigeben.</span><span class="sxs-lookup"><span data-stu-id="bab0d-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="bab0d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bab0d-140">Requirements</span></span>



| <span data-ttu-id="bab0d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bab0d-141">Requirement</span></span> | <span data-ttu-id="bab0d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="bab0d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bab0d-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bab0d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bab0d-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bab0d-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bab0d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bab0d-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bab0d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bab0d-147">Header</span><span class="sxs-lookup"><span data-stu-id="bab0d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="bab0d-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab0d-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="bab0d-149">IDL</span><span class="sxs-lookup"><span data-stu-id="bab0d-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bab0d-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bab0d-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 

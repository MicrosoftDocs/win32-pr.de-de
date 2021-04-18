---
description: 'Die IWiaDevMgr2:: getimagedlg-Methode zeigt ein oder mehrere Dialogfelder an, mit denen ein Benutzer ein Bild von einem Windows-Image Erfassungsgerät (WIA) 2,0 abrufen und in eine angegebene Datei schreiben kann.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2:: getimagedlg-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359060"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="35e48-103">IWiaDevMgr2:: getimagedlg-Methode</span><span class="sxs-lookup"><span data-stu-id="35e48-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="35e48-104">Die **IWiaDevMgr2:: getimagedlg** -Methode zeigt ein oder mehrere Dialogfelder an, mit denen ein Benutzer ein Bild von einem Windows-Image Erfassungsgerät (WIA) 2,0 abrufen und in eine angegebene Datei schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="35e48-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="35e48-105">Mit dieser Methode wird die Funktionalität von [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) erweitert, um die Bild Erfassung innerhalb eines einzelnen API-Aufrufs zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="35e48-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e48-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e48-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="35e48-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="35e48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e48-108">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-109">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="35e48-109">Type: **LONG**</span></span>

<span data-ttu-id="35e48-110">Gibt das Dialogfeld Verhalten an.</span><span class="sxs-lookup"><span data-stu-id="35e48-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="35e48-111">Kann auf die folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="35e48-111">Can be set to the following values:</span></span>



| <span data-ttu-id="35e48-112">Flag</span><span class="sxs-lookup"><span data-stu-id="35e48-112">Flag</span></span>                                 | <span data-ttu-id="35e48-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="35e48-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e48-114">0</span><span class="sxs-lookup"><span data-stu-id="35e48-114">0</span></span>                                    | <span data-ttu-id="35e48-115">Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="35e48-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="35e48-116">Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="35e48-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="35e48-117">Verwenden Sie die Benutzeroberfläche des-Systems anstelle der vom Hersteller bereitgestellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="35e48-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="35e48-118">Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="35e48-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="35e48-119">Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="35e48-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="35e48-120">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-121">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35e48-121">Type: **BSTR**</span></span>

<span data-ttu-id="35e48-122">Gibt den zu verwendenden Scanner an.</span><span class="sxs-lookup"><span data-stu-id="35e48-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="35e48-123">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-124">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="35e48-124">Type: **HWND**</span></span>

<span data-ttu-id="35e48-125">Ein Handle des Fensters, das das Dialogfeld " **Bild Abbild** " besitzt.</span><span class="sxs-lookup"><span data-stu-id="35e48-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="35e48-126">*bstrinfoldername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-127">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35e48-127">Type: **BSTR**</span></span>

<span data-ttu-id="35e48-128">Gibt den Namen des Ordners an, in dem die gescannten Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="35e48-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="35e48-129">*bstrauch filename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-130">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35e48-130">Type: **BSTR**</span></span>

<span data-ttu-id="35e48-131">Gibt den Namen der Datei an, in die die Bilddaten geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="35e48-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="35e48-132">*plnumfiles* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-133">Type: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="35e48-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="35e48-134">Ein Zeiger auf die Anzahl der zu überprüfenden Dateien.</span><span class="sxs-lookup"><span data-stu-id="35e48-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="35e48-135">_ppbstrFilePaths \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e48-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-136">Typ: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="35e48-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="35e48-137">Die Adresse eines Zeigers auf ein Array von Pfaden für die gescannten Dateien.</span><span class="sxs-lookup"><span data-stu-id="35e48-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="35e48-138">Initialisieren Sie den Zeiger so, dass er auf ein Array der Größe 0 (null) verweist, bevor **IWiaDevMgr2:: getimagedlg** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35e48-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="35e48-139">Siehe **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="35e48-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="35e48-140">*ppitem* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35e48-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35e48-141">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="35e48-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="35e48-142">Die Adresse eines Zeigers auf den [**IWiaItem2**](-wia-iwiaitem2.md) , von dem die Bilder gescannt wurden.</span><span class="sxs-lookup"><span data-stu-id="35e48-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e48-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35e48-143">Return value</span></span>

<span data-ttu-id="35e48-144">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="35e48-144">Type: **HRESULT**</span></span>

<span data-ttu-id="35e48-145">**IWiaDevMgr2:: getimagedlg** gibt "s OK" zurück \_ , wenn die Daten erfolgreich übertragen werden, gibt "false" zurück, \_ Wenn der Benutzer das Dialogfeld abbricht, oder gibt einen com-Standardfehler zurück.</span><span class="sxs-lookup"><span data-stu-id="35e48-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="35e48-146">Der *ppbstraufilepath* -Parameter ist nicht notwendigerweise leer, wenn die Funktion "S false" zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="35e48-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="35e48-147">Wenn der Benutzer abbricht, werden die Seiten, bei denen die Überprüfung abgeschlossen ist, verarbeitet und in *ppbstraufilepath* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35e48-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="35e48-148">Auch wenn Sie nicht verwendet werden, müssen Sie das Array freigeben.</span><span class="sxs-lookup"><span data-stu-id="35e48-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="35e48-149">Siehe **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="35e48-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="35e48-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35e48-150">Remarks</span></span>

<span data-ttu-id="35e48-151">Wenn die Anwendung für den Wert des Parameters *bstraude viceid* den Wert **null** übergibt, zeigt **IWiaDevMgr2:: getimagetimagedlg** das Dialogfeld **Gerät auswählen** an, sodass der Benutzer das WIA 2,0-Eingabegerät auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="35e48-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="35e48-152">Verwenden Sie im Menü **Datei** ein Menü Element mit dem Namen **aus Scanner** , damit die Geräte-und Image Auswahl in der Anwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="35e48-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="35e48-153">Nennen Sie [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) auf jedem BSTR im Array, auf das *ppbstraufilepath* \[ \] verweist, und nennen Sie " [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " für das Array selbst, um zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="35e48-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="35e48-154">Wenn S \_ false zurückgegeben wird, überprüfen Sie, ob der Wert, auf den *plnumfiles* verweist, nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="35e48-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="35e48-155">Wenn der Wert nicht NULL ist, können Sie die Ressourcen von *ppbtrefilepath* \[ i \] in der Anwendung freigeben, da der Benutzer nach dem Scannen einer oder mehrerer Seiten abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="35e48-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="35e48-156">Initialisieren Sie *plnumfiles* mit 0 (null), bevor Sie **IWiaDevMgr2:: getimagedlg** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="35e48-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="35e48-157">Wenn *plnumfiles* nicht mit 0 (null) initialisiert wird und ein Fehler in der com-Infrastruktur bewirkt, dass die Funktion den Wert "false" zurückgibt \_ , bevor **IWiaDevMgr2:: getimagedlg** aufgerufen wird, weist *plnumfiles* einen irreführenden Garbage-Wert auf.</span><span class="sxs-lookup"><span data-stu-id="35e48-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="35e48-158">Das Dialogfeld muss über ausreichende Berechtigungen für *bstrinfoldername* verfügen, damit die Dateien mit eindeutigen Dateinamen gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="35e48-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="35e48-159">Schützen Sie den Ordner mit einer Zugriffs Steuerungs Liste (Access Control List, ACL), da er Benutzerdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="35e48-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e48-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35e48-160">Requirements</span></span>



| <span data-ttu-id="35e48-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35e48-161">Requirement</span></span> | <span data-ttu-id="35e48-162">Wert</span><span class="sxs-lookup"><span data-stu-id="35e48-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="35e48-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35e48-163">Minimum supported client</span></span><br/> | <span data-ttu-id="35e48-164">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35e48-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35e48-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35e48-165">Minimum supported server</span></span><br/> | <span data-ttu-id="35e48-166">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35e48-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35e48-167">Header</span><span class="sxs-lookup"><span data-stu-id="35e48-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="35e48-168"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="35e48-168"><dt>Wia.h</dt></span></span> </dl> |



 

 

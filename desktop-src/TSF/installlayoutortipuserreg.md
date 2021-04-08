---
title: Installlayoutortipuserreg-Funktion
description: Aktiviert die angegebenen Tastaturlayouts oder Text Dienste für den angegebenen Benutzer.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Installlayoutortipuserreg-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741625"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="9dec0-104">Installlayoutortipuserreg-Funktion</span><span class="sxs-lookup"><span data-stu-id="9dec0-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="9dec0-105">Aktiviert die angegebenen Tastaturlayouts oder Text Dienste für den angegebenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9dec0-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dec0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dec0-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9dec0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dec0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dec0-108">*pszuserreg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9dec0-109">Der Registrierungs Pfad des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9dec0-109">The registry path of the user.</span></span> <span data-ttu-id="9dec0-110">Wenn dieser Parameter **null** ist, wird der aktuelle HKEY- \_ \_ Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dec0-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="9dec0-111">*pszsystemreg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9dec0-112">Der Registrierungs Pfad des Systems.</span><span class="sxs-lookup"><span data-stu-id="9dec0-112">The registry path of the system.</span></span> <span data-ttu-id="9dec0-113">Wenn dieser Parameter **null** ist, wird HKEY \_ local \_ Machine \\ System verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dec0-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="9dec0-114">*pszsoftwarerereg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9dec0-115">Der Registrierungs Pfad der Software.</span><span class="sxs-lookup"><span data-stu-id="9dec0-115">The registry path of the software.</span></span> <span data-ttu-id="9dec0-116">Wenn dieser Parameter **null** ist, wird die lokale HKEY- \_ \_ Computer \\ Software verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dec0-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="9dec0-117">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dec0-118">Eine Zeichenfolge, die die Liste der Tastaturlayout-oder Text Dienst profile darstellt.</span><span class="sxs-lookup"><span data-stu-id="9dec0-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="9dec0-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dec0-120">Ein Bitfeld, das die folgenden Flags angibt.</span><span class="sxs-lookup"><span data-stu-id="9dec0-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="9dec0-121">Die folgenden Bezeichner sind nicht in einer öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="9dec0-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="9dec0-122">Sie müssen entweder den Hexadezimalwert verwenden oder die Bezeichner \# definieren.</span><span class="sxs-lookup"><span data-stu-id="9dec0-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="9dec0-123">Wenn Sie z. b. " **Ilot \_ Uninstall** " verwenden möchten, müssen Sie `#define ILOT_UNINSTALL 0x00000001` in Ihren Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="9dec0-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="9dec0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9dec0-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="9dec0-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9dec0-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="9dec0-126"><dt>**Ilot \_**</dt> <dt>0x00000001</dt> deinstallieren</span><span class="sxs-lookup"><span data-stu-id="9dec0-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="9dec0-127">Identisch mit " **Ilot \_ deaktiviert**".</span><span class="sxs-lookup"><span data-stu-id="9dec0-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="9dec0-128"><dt>**Ilot \_ Defprofile**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="9dec0-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="9dec0-129">Legt das angegebene Layout oder den Tipp als Standardelement fest.</span><span class="sxs-lookup"><span data-stu-id="9dec0-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="9dec0-130"><dt>**Ilot \_ Noapplydecurrentsession**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="9dec0-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="9dec0-131">Die Einstellung wird gespeichert, aber nicht auf die aktuelle Sitzung angewendet.</span><span class="sxs-lookup"><span data-stu-id="9dec0-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="9dec0-132"><dt>**Ilot \_ Cleaninstall**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="9dec0-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="9dec0-133">Deaktiviert alle aktuellen Tastaturlayouts und Text Dienste.</span><span class="sxs-lookup"><span data-stu-id="9dec0-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="9dec0-134"><dt>**Ilot \_**</dt> <dt>0x00000080</dt> deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9dec0-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="9dec0-135">Deaktiviert das angegebene Tastaturlayout und den angegebenen Text Dienst.</span><span class="sxs-lookup"><span data-stu-id="9dec0-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dec0-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dec0-136">Return value</span></span>



| <span data-ttu-id="9dec0-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9dec0-137">Return code</span></span>                                                                         | <span data-ttu-id="9dec0-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dec0-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9dec0-139"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="9dec0-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="9dec0-140">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9dec0-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="9dec0-141"><dt>**-Sicherung**</dt></span><span class="sxs-lookup"><span data-stu-id="9dec0-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="9dec0-142">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9dec0-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9dec0-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dec0-143">Remarks</span></span>

<span data-ttu-id="9dec0-144">Das Zeichen folgen Format der Layoutliste lautet:</span><span class="sxs-lookup"><span data-stu-id="9dec0-144">The string format of the layout list is:</span></span>

<span data-ttu-id="9dec0-145"><langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="9dec0-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="9dec0-146">Das Zeichen folgen Format der Text Dienst Profil Liste lautet:</span><span class="sxs-lookup"><span data-stu-id="9dec0-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="9dec0-147"><langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="9dec0-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="9dec0-148">Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="9dec0-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="9dec0-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dec0-149">Examples</span></span>

<span data-ttu-id="9dec0-150">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9dec0-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="9dec0-151">Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9dec0-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="9dec0-152">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="9dec0-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="9dec0-153">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="9dec0-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="9dec0-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dec0-154">Requirements</span></span>



| <span data-ttu-id="9dec0-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dec0-155">Requirement</span></span> | <span data-ttu-id="9dec0-156">Wert</span><span class="sxs-lookup"><span data-stu-id="9dec0-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9dec0-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dec0-157">Minimum supported client</span></span><br/> | <span data-ttu-id="9dec0-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9dec0-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dec0-159">Minimum supported server</span></span><br/> | <span data-ttu-id="9dec0-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dec0-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9dec0-161">DLL</span><span class="sxs-lookup"><span data-stu-id="9dec0-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dec0-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dec0-162"><dt>Input.dll</dt></span></span> </dl> |



 


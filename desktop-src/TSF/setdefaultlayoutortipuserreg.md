---
title: Setdefaultlayoutortipuserreg-Funktion
description: Legt das angegebene Tastaturlayout oder einen Text Dienst als Standardeingabe Element der Benutzerregistrierung fest.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Setdefaultlayoutortipuserreg Function-Framework für Text Dienste
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103018"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="7a517-104">Setdefaultlayoutortipuserreg-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a517-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="7a517-105">Legt das angegebene Tastaturlayout oder einen Text Dienst als Standardeingabe Element der Benutzerregistrierung fest.</span><span class="sxs-lookup"><span data-stu-id="7a517-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a517-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a517-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7a517-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a517-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a517-108">*pszuserreg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7a517-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a517-109">Der Registrierungs Pfad des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a517-109">The registry path of the user.</span></span> <span data-ttu-id="7a517-110">Wenn dieser Parameter **null** ist, wird der aktuelle HKEY- \_ \_ Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a517-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="7a517-111">*pszsystemreg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7a517-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a517-112">Der Registrierungs Pfad des Systems.</span><span class="sxs-lookup"><span data-stu-id="7a517-112">The registry path of the system.</span></span> <span data-ttu-id="7a517-113">Wenn dieser Parameter **null** ist, wird HKEY \_ local \_ Machine \\ System verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a517-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="7a517-114">*pszsoftwarerereg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7a517-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a517-115">Der Registrierungs Pfad der Software.</span><span class="sxs-lookup"><span data-stu-id="7a517-115">The registry path of the software.</span></span> <span data-ttu-id="7a517-116">Wenn dieser Parameter **null** ist, wird die lokale HKEY- \_ \_ Computer \\ Software verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a517-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="7a517-117">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a517-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a517-118">Eine Zeichenfolge, die die Liste der Tastaturlayout-oder Text Dienst profile darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a517-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="7a517-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a517-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a517-120">Ein Bitfeld, das die folgenden Flags angibt:</span><span class="sxs-lookup"><span data-stu-id="7a517-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="7a517-121">Die folgenden Bezeichner sind nicht in einer öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="7a517-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="7a517-122">Sie müssen entweder den Hexadezimalwert verwenden oder die Bezeichner \# definieren.</span><span class="sxs-lookup"><span data-stu-id="7a517-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="7a517-123">Wenn Sie z. b. "sdlot \_ noapplydecurrentsession" verwenden möchten, müssen Sie " \# sdlot \_ noapplydecurrentsession 0x00000001" in Ihren Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="7a517-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="7a517-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7a517-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="7a517-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7a517-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="7a517-126"><dt>**Sdlot \_ Noapplydecurrentsession**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7a517-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7a517-127">Speichert die Einstellung in der Registrierung, aber die Lauf Zeit Tastatur Einstellung der aktuellen Sitzung wird nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7a517-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="7a517-128">Wenn der Alternative Registrierungs Pfad in **setdefaultlayoutor tipuserreg** festgelegt wird, sollte dieses Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a517-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="7a517-129"><dt>**Sdlot \_ Applyycurrentthread**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7a517-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="7a517-130">Wendet die Einstellung direkt auf den aktuellen Thread an.</span><span class="sxs-lookup"><span data-stu-id="7a517-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a517-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a517-131">Return value</span></span>



| <span data-ttu-id="7a517-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7a517-132">Return code</span></span>                                                                          | <span data-ttu-id="7a517-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a517-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7a517-134"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="7a517-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="7a517-135">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7a517-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="7a517-136"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="7a517-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="7a517-137">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7a517-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a517-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a517-138">Remarks</span></span>

<span data-ttu-id="7a517-139">Das Zeichen folgen Format der Layoutliste lautet:</span><span class="sxs-lookup"><span data-stu-id="7a517-139">The string format of the layout list is:</span></span>

<span data-ttu-id="7a517-140"><langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="7a517-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="7a517-141">Das Zeichen folgen Format der Text Dienst Profil Liste lautet:</span><span class="sxs-lookup"><span data-stu-id="7a517-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="7a517-142"><langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="7a517-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="7a517-143">Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="7a517-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="7a517-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a517-144">Examples</span></span>

<span data-ttu-id="7a517-145">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7a517-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="7a517-146">Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7a517-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="7a517-147">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="7a517-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="7a517-148">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="7a517-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="7a517-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a517-149">Requirements</span></span>



| <span data-ttu-id="7a517-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a517-150">Requirement</span></span> | <span data-ttu-id="7a517-151">Wert</span><span class="sxs-lookup"><span data-stu-id="7a517-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a517-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a517-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7a517-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a517-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7a517-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a517-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7a517-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a517-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a517-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7a517-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a517-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a517-157"><dt>Input.dll</dt></span></span> </dl> |



 


---
title: Installlayoutortip-Funktion
description: Aktiviert die angegebenen Tastaturlayouts oder Text Dienste.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- Installlayoutortip-Funktion Text Services-Framework
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339574"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="099af-104">Installlayoutortip-Funktion</span><span class="sxs-lookup"><span data-stu-id="099af-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="099af-105">Aktiviert die angegebenen Tastaturlayouts oder Text Dienste.</span><span class="sxs-lookup"><span data-stu-id="099af-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="099af-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="099af-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="099af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="099af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099af-108">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="099af-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099af-109">Eine Zeichenfolge, die die Liste der Tastaturlayout-oder Text Dienst profile darstellt.</span><span class="sxs-lookup"><span data-stu-id="099af-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="099af-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="099af-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099af-111">Ein Bitfeld, das die folgenden Flags angibt:</span><span class="sxs-lookup"><span data-stu-id="099af-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="099af-112">Die folgenden Bezeichner sind nicht in einer öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="099af-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="099af-113">Sie müssen entweder den Hexadezimalwert verwenden oder die Bezeichner \# definieren.</span><span class="sxs-lookup"><span data-stu-id="099af-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="099af-114">Wenn Sie z. b. " **Ilot \_ Uninstall** " verwenden möchten, müssen Sie `#define ILOT_UNINSTALL 0x00000001` in Ihren Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="099af-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="099af-115">Wert</span><span class="sxs-lookup"><span data-stu-id="099af-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="099af-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="099af-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="099af-117"><dt>**Ilot \_**</dt> <dt>0x00000001</dt> deinstallieren</span><span class="sxs-lookup"><span data-stu-id="099af-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="099af-118">Identisch mit " **Ilot \_ deaktiviert**".</span><span class="sxs-lookup"><span data-stu-id="099af-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="099af-119"><dt>**Ilot \_ Defprofile**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="099af-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="099af-120">Legt das angegebene Layout oder den Tipp als Standardelement fest.</span><span class="sxs-lookup"><span data-stu-id="099af-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="099af-121"><dt>**Ilot \_ DEFUSER4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="099af-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="099af-122">Ändert die Einstellung von. Vorgegebene.</span><span class="sxs-lookup"><span data-stu-id="099af-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="099af-123"><dt>**Ilot \_ Syslocale**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="099af-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="099af-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="099af-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="099af-125"><dt>**Ilot \_ Nolocaletoenumerate**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="099af-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="099af-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="099af-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="099af-127"><dt>**Ilot \_ Noapplydecurrentsession**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="099af-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="099af-128">Die Einstellung wird gespeichert, aber nicht auf die aktuelle Sitzung angewendet.</span><span class="sxs-lookup"><span data-stu-id="099af-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="099af-129"><dt>**Ilot \_ Cleaninstall**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="099af-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="099af-130">Deaktiviert alle aktuellen Tastaturlayouts und Text Dienste.</span><span class="sxs-lookup"><span data-stu-id="099af-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="099af-131"><dt>**Ilot \_**</dt> <dt>0x00000080</dt> deaktiviert</span><span class="sxs-lookup"><span data-stu-id="099af-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="099af-132">Deaktiviert das angegebene Tastaturlayout und den angegebenen Text Dienst.</span><span class="sxs-lookup"><span data-stu-id="099af-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099af-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="099af-133">Return value</span></span>



| <span data-ttu-id="099af-134">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="099af-134">Return code</span></span>                                                                          | <span data-ttu-id="099af-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="099af-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="099af-136"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="099af-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="099af-137">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="099af-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="099af-138"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="099af-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="099af-139">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="099af-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="099af-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="099af-140">Remarks</span></span>

<span data-ttu-id="099af-141">Das Zeichen folgen Format der Layoutliste lautet:</span><span class="sxs-lookup"><span data-stu-id="099af-141">The string format of the layout list is:</span></span>

<span data-ttu-id="099af-142"><langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="099af-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="099af-143">Das Zeichen folgen Format der Text Dienst Profil Liste lautet:</span><span class="sxs-lookup"><span data-stu-id="099af-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="099af-144"><langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="099af-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="099af-145">Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="099af-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="099af-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="099af-146">Examples</span></span>

<span data-ttu-id="099af-147">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="099af-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="099af-148">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="099af-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="099af-149">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="099af-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="099af-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="099af-150">Requirements</span></span>



| <span data-ttu-id="099af-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="099af-151">Requirement</span></span> | <span data-ttu-id="099af-152">Wert</span><span class="sxs-lookup"><span data-stu-id="099af-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="099af-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="099af-153">Minimum supported client</span></span><br/> | <span data-ttu-id="099af-154">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="099af-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="099af-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="099af-155">Minimum supported server</span></span><br/> | <span data-ttu-id="099af-156">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="099af-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="099af-157">DLL</span><span class="sxs-lookup"><span data-stu-id="099af-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="099af-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="099af-158"><dt>Input.dll</dt></span></span> </dl> |



 


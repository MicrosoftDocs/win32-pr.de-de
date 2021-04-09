---
title: Setdefaultlayoutortip-Funktion
description: Legt das angegebene Tastaturlayout oder einen Text Dienst als Standardeingabe Element des aktuellen Benutzers fest.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Setdefaultlayoutortip-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103194"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="ecb03-104">Setdefaultlayoutortip-Funktion</span><span class="sxs-lookup"><span data-stu-id="ecb03-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="ecb03-105">Legt das angegebene Tastaturlayout oder einen Text Dienst als Standardeingabe Element des aktuellen Benutzers fest.</span><span class="sxs-lookup"><span data-stu-id="ecb03-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb03-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecb03-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ecb03-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecb03-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb03-108">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecb03-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb03-109">Eine Zeichenfolge, die eine Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ecb03-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="ecb03-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecb03-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb03-111">Ein Bitfeld, das die folgenden Flags angibt.</span><span class="sxs-lookup"><span data-stu-id="ecb03-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="ecb03-112">Die folgenden Bezeichner sind nicht in einer öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="ecb03-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="ecb03-113">Sie müssen entweder den Hexadezimalwert verwenden oder die Bezeichner \# definieren.</span><span class="sxs-lookup"><span data-stu-id="ecb03-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="ecb03-114">Wenn Sie z. b. "sdlot \_ noapplydecurrentsession" verwenden möchten, müssen Sie " \# sdlot \_ noapplydecurrentsession 0x00000001" in Ihren Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="ecb03-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="ecb03-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ecb03-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="ecb03-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ecb03-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="ecb03-117"><dt>**Sdlot \_ Noapplydecurrentsession**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ecb03-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ecb03-118">Speichert die Einstellung in der Registrierung, aber die Lauf Zeit Tastatur Einstellung der aktuellen Sitzung wird nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ecb03-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="ecb03-119">Wenn der Alternative Registrierungs Pfad in [**setdefaultlayoutor tipuserreg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg)festgelegt wird, sollte dieses Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb03-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="ecb03-120"><dt>**Sdlot \_ Applyycurrentthread**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ecb03-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="ecb03-121">Wendet die Einstellung direkt auf den aktuellen Thread an.</span><span class="sxs-lookup"><span data-stu-id="ecb03-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb03-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecb03-122">Return value</span></span>



| <span data-ttu-id="ecb03-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ecb03-123">Return code</span></span>                                                                          | <span data-ttu-id="ecb03-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecb03-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ecb03-125"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb03-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="ecb03-126">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ecb03-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="ecb03-127"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb03-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="ecb03-128">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ecb03-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ecb03-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecb03-129">Remarks</span></span>

<span data-ttu-id="ecb03-130">Das Zeichen folgen Format der Layoutliste lautet:</span><span class="sxs-lookup"><span data-stu-id="ecb03-130">The string format of the layout list is:</span></span>

<span data-ttu-id="ecb03-131"><langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="ecb03-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="ecb03-132">Das Zeichen folgen Format der Text Dienst Profil Liste lautet:</span><span class="sxs-lookup"><span data-stu-id="ecb03-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="ecb03-133"><langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="ecb03-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="ecb03-134">Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="ecb03-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="ecb03-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecb03-135">Examples</span></span>

<span data-ttu-id="ecb03-136">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ecb03-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="ecb03-137">Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ecb03-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="ecb03-138">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ecb03-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="ecb03-139">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="ecb03-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="ecb03-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecb03-140">Requirements</span></span>



| <span data-ttu-id="ecb03-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecb03-141">Requirement</span></span> | <span data-ttu-id="ecb03-142">Wert</span><span class="sxs-lookup"><span data-stu-id="ecb03-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb03-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecb03-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb03-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecb03-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ecb03-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecb03-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb03-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecb03-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ecb03-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb03-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb03-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb03-148"><dt>Input.dll</dt></span></span> </dl> |



 


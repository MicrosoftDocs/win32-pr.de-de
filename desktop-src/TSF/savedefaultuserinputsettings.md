---
title: Savedefaultuserinputsettings-Funktion
description: Wendet die Benutzer Tastaturlayout-und Text Dienst Einstellung auf die Standardbenutzer Struktur an.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- Savedefaultuserinputsettings-Funktion, Text Dienste-Framework
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391700"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="5eaf8-104">Savedefaultuserinputsettings-Funktion</span><span class="sxs-lookup"><span data-stu-id="5eaf8-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="5eaf8-105">Wendet die Benutzer Tastaturlayout-und Text Dienst Einstellung auf die Standardbenutzer Struktur an.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eaf8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eaf8-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="5eaf8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5eaf8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eaf8-108">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eaf8-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eaf8-109">Das übergeordnete Fenster für das Dialogfeld "Warnung".</span><span class="sxs-lookup"><span data-stu-id="5eaf8-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="5eaf8-110">Das Dialogfeld "Warnung" wird nicht immer angezeigt und wird entsprechend angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="5eaf8-111">Wenn dieser Parameter NULL ist, wird das Dialogfeld Warnung nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="5eaf8-112">*hsourceregkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eaf8-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eaf8-113">Der Stamm Registrierungsschlüssel der zu kopierenden Benutzereinstellung.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eaf8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5eaf8-114">Return value</span></span>



| <span data-ttu-id="5eaf8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5eaf8-115">Return code</span></span>                                                                          | <span data-ttu-id="5eaf8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5eaf8-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5eaf8-117"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="5eaf8-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="5eaf8-118">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="5eaf8-119"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="5eaf8-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="5eaf8-120">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5eaf8-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5eaf8-121">Examples</span></span>

<span data-ttu-id="5eaf8-122">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="5eaf8-123">Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="5eaf8-124">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5eaf8-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="5eaf8-125">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="5eaf8-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="5eaf8-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eaf8-126">Requirements</span></span>



| <span data-ttu-id="5eaf8-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eaf8-127">Requirement</span></span> | <span data-ttu-id="5eaf8-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5eaf8-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5eaf8-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5eaf8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5eaf8-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eaf8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5eaf8-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5eaf8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5eaf8-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eaf8-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5eaf8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5eaf8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eaf8-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eaf8-134"><dt>Input.dll</dt></span></span> </dl> |



 


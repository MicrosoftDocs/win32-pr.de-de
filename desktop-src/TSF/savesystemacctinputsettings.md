---
title: Savesystemacctinputsettings-Funktion
description: Wendet das Layout der Benutzer Tastatur und den Text Dienst auf die Hive des System Kontos an.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Savesystemacctinputsettings-Funktion, Text Dienste-Framework
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391568"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="d36f6-104">Savesystemacctinputsettings-Funktion</span><span class="sxs-lookup"><span data-stu-id="d36f6-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="d36f6-105">Wendet das Layout der Benutzer Tastatur und den Text Dienst auf die Hive des System Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d36f6-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36f6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d36f6-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="d36f6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d36f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36f6-108">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d36f6-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d36f6-109">Das übergeordnete Fenster für das Dialogfeld "Warnung".</span><span class="sxs-lookup"><span data-stu-id="d36f6-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="d36f6-110">Das Dialogfeld "Warnung" wird nicht immer angezeigt und wird entsprechend angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d36f6-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="d36f6-111">Wenn dieser Parameter **null** ist, wird das Dialogfeld Warnung nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d36f6-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="d36f6-112">*hsourceregkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d36f6-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d36f6-113">Der Stamm Registrierungsschlüssel der zu kopierenden Benutzereinstellung.</span><span class="sxs-lookup"><span data-stu-id="d36f6-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36f6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d36f6-114">Return value</span></span>



| <span data-ttu-id="d36f6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d36f6-115">Return code</span></span>                                                                          | <span data-ttu-id="d36f6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d36f6-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d36f6-117"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="d36f6-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="d36f6-118">Die Funktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d36f6-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="d36f6-119"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="d36f6-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="d36f6-120">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d36f6-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d36f6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d36f6-121">Remarks</span></span>

<span data-ttu-id="d36f6-122">Die Systemkonto Struktur ist HKEY- \_ Benutzer \\ . Standard, HKEY \_ \\ -Benutzer s-1-5-19 und HKEY \_ \\ -Benutzer s-1-5-20.</span><span class="sxs-lookup"><span data-stu-id="d36f6-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="d36f6-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d36f6-123">Examples</span></span>

<span data-ttu-id="d36f6-124">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d36f6-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="d36f6-125">Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d36f6-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="d36f6-126">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d36f6-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="d36f6-127">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="d36f6-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="d36f6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d36f6-128">Requirements</span></span>



| <span data-ttu-id="d36f6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d36f6-129">Requirement</span></span> | <span data-ttu-id="d36f6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d36f6-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d36f6-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d36f6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d36f6-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d36f6-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d36f6-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d36f6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d36f6-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d36f6-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d36f6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d36f6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d36f6-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d36f6-136"><dt>Input.dll</dt></span></span> </dl> |



 


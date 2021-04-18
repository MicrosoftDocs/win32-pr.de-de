---
title: Enumlayoutortipforsetup-Funktion
description: Listet die installierten Tastaturlayouts und Text Dienste der Setup Benutzeroberfläche oder des OOBE-Werts auf.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Enumlayoutortipforsetup-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338528"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="1c5d4-104">Enumlayoutortipforsetup-Funktion</span><span class="sxs-lookup"><span data-stu-id="1c5d4-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="1c5d4-105">Listet die installierten Tastaturlayouts und Text Dienste der Setup Benutzeroberfläche oder des OOBE-Werts auf.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c5d4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c5d4-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1c5d4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c5d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c5d4-108">*LangID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c5d4-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5d4-109">Die Sprach-ID des Elements, das aufgelistet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="1c5d4-110">*playoutor Tip* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1c5d4-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5d4-111">Zeiger auf den Puffer, der das Array der layoutor Tip-Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="1c5d4-112">Dies kann **null** sein, um die Anzahl der Elemente zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="1c5d4-113">*ubuflength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c5d4-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5d4-114">Die Länge des Puffers, auf den von *playoutor Tip* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="1c5d4-115">Dies wird ignoriert, wenn *playoutor Tip* den Wert **null** hat.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1c5d4-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c5d4-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5d4-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-117">Not used.</span></span> <span data-ttu-id="1c5d4-118">Dieser Wert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c5d4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c5d4-119">Return value</span></span>

<span data-ttu-id="1c5d4-120">Wenn *playoutor Tip* **null** ist, wird die Anzahl von Tastatur Elementen, die im System registriert sind, angezeigt. andernfalls die Anzahl der Tastatur Elemente, die in " *playoutor Tip*" kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c5d4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c5d4-121">Remarks</span></span>

<span data-ttu-id="1c5d4-122">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="1c5d4-123">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="1c5d4-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="1c5d4-124">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="1c5d4-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="1c5d4-125">Die Definition von layoutor Tip lautet:</span><span class="sxs-lookup"><span data-stu-id="1c5d4-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="1c5d4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c5d4-126">Requirements</span></span>



| <span data-ttu-id="1c5d4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c5d4-127">Requirement</span></span> | <span data-ttu-id="1c5d4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1c5d4-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5d4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c5d4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5d4-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c5d4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1c5d4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c5d4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5d4-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c5d4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1c5d4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1c5d4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c5d4-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c5d4-134"><dt>Input.dll</dt></span></span> </dl> |



 


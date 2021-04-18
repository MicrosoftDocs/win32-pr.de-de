---
title: Enumenabledlayoutortip-Funktion
description: Listet alle aktivierten Tastaturlayouts oder Text Dienste der angegebenen Benutzereinstellung auf.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Enumenabledlayoutortip-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340786"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="2ebec-104">Enumenabledlayoutortip-Funktion</span><span class="sxs-lookup"><span data-stu-id="2ebec-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="2ebec-105">Listet alle aktivierten Tastaturlayouts oder Text Dienste der angegebenen Benutzereinstellung auf.</span><span class="sxs-lookup"><span data-stu-id="2ebec-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ebec-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="2ebec-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ebec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ebec-108">*pszuserreg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebec-109">Der Registrierungs Pfad des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2ebec-109">The registry path of the user.</span></span> <span data-ttu-id="2ebec-110">Wenn dieser Parameter **null** ist, wird der aktuelle HKEY- \_ \_ Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ebec-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="2ebec-111">*pszsystemreg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebec-112">Der Registrierungs Pfad des Systems.</span><span class="sxs-lookup"><span data-stu-id="2ebec-112">The registry path of the system.</span></span> <span data-ttu-id="2ebec-113">Wenn dieser Parameter **null** ist, wird HKEY \_ local \_ Machine \\ System verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ebec-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="2ebec-114">*pszsoftwarerereg* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebec-115">Der Registrierungs Pfad der Software.</span><span class="sxs-lookup"><span data-stu-id="2ebec-115">The registry path of the software.</span></span> <span data-ttu-id="2ebec-116">Wenn dieser Parameter **null** ist, wird die lokale HKEY- \_ \_ Computer \\ Software verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ebec-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="2ebec-117">*playoutor-Profil* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebec-118">Zeiger auf den Puffer, der das layoutor profile-Array empfängt.</span><span class="sxs-lookup"><span data-stu-id="2ebec-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="2ebec-119">*ubuflength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebec-120">Die Länge des Puffers, auf den von *playoutor Tip profile* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2ebec-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ebec-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ebec-121">Return value</span></span>

<span data-ttu-id="2ebec-122">Wenn " *playoutor tipprofile* " **null** ist, wird die Anzahl der in der Benutzereinstellung aktivierten Tastatur Elemente angezeigt. andernfalls die Anzahl der Tastatur Elemente, die in *playoutor profile* kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="2ebec-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="2ebec-123">Für IME-Sprachen (Input Method Editor) werden alle IMEs zurückgegeben, auch wenn nur ein IME aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ebec-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="2ebec-124">Wenn für einen Benutzer z. b. die Schnelleingabe Taste "cht New" aktiviert ist, gibt die **enumenabledlayoutortip** -Funktion alle fünf cht-IDs zurück.</span><span class="sxs-lookup"><span data-stu-id="2ebec-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ebec-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ebec-125">Remarks</span></span>

<span data-ttu-id="2ebec-126">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ebec-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="2ebec-127">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="2ebec-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="2ebec-128">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="2ebec-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="2ebec-129">Die Definition von layoutor profile lautet:</span><span class="sxs-lookup"><span data-stu-id="2ebec-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="2ebec-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ebec-130">Requirements</span></span>



| <span data-ttu-id="2ebec-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ebec-131">Requirement</span></span> | <span data-ttu-id="2ebec-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2ebec-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebec-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ebec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebec-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2ebec-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ebec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebec-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ebec-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ebec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2ebec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ebec-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ebec-138"><dt>Input.dll</dt></span></span> </dl> |



 


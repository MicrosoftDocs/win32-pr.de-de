---
description: Öffnet das Dialogfeld "Schlüssel-Manager" in der Benutzeroberfläche.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364794"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="f91ff-103">KRShowKeyMgr-Funktion</span><span class="sxs-lookup"><span data-stu-id="f91ff-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="f91ff-104">\[Diese Funktion ist nur in Windows XP enthalten.</span><span class="sxs-lookup"><span data-stu-id="f91ff-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="f91ff-105">Es ist zurzeit nicht in einer anderen Version von Windows enthalten, und es wird davon ausgegangen, dass es in zukünftigen Versionen von Windows nicht mehr enthalten ist.\]</span><span class="sxs-lookup"><span data-stu-id="f91ff-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="f91ff-106">Öffnet das Dialogfeld "Schlüssel-Manager" in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f91ff-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f91ff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f91ff-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="f91ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f91ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f91ff-109">*hwparent*</span><span class="sxs-lookup"><span data-stu-id="f91ff-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="f91ff-110">Ein Handle für das übergeordnete Fenster des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="f91ff-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="f91ff-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="f91ff-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f91ff-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="f91ff-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f91ff-113">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f91ff-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f91ff-114">*pszcmdline*</span><span class="sxs-lookup"><span data-stu-id="f91ff-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="f91ff-115">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f91ff-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f91ff-116">*Cmdshow*</span><span class="sxs-lookup"><span data-stu-id="f91ff-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="f91ff-117">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f91ff-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f91ff-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f91ff-118">Return value</span></span>

<span data-ttu-id="f91ff-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f91ff-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f91ff-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f91ff-120">Remarks</span></span>

<span data-ttu-id="f91ff-121">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f91ff-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f91ff-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f91ff-122">Requirements</span></span>



| <span data-ttu-id="f91ff-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f91ff-123">Requirement</span></span> | <span data-ttu-id="f91ff-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f91ff-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f91ff-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f91ff-125">DLL</span></span><br/> | <dl> <span data-ttu-id="f91ff-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f91ff-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 

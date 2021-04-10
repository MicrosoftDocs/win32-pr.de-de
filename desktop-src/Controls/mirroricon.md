---
title: Mirroricon-Funktion
description: Kehrt Symbole (Spiegelung) so um, dass Sie ordnungsgemäß in einem gespiegelten Gerätekontext angezeigt werden.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Windows-Steuerelemente der mirroricon-Funktion
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040237"
---
# <a name="mirroricon-function"></a><span data-ttu-id="c03b3-104">Mirroricon-Funktion</span><span class="sxs-lookup"><span data-stu-id="c03b3-104">MirrorIcon function</span></span>

<span data-ttu-id="c03b3-105">\[**Mirroricon** ist über Windows XP mit Service Pack 2 (SP2) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c03b3-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="c03b3-106">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c03b3-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c03b3-107">Kehrt Symbole (Spiegelung) so um, dass Sie ordnungsgemäß in einem gespiegelten Gerätekontext angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c03b3-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c03b3-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="c03b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c03b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03b3-110">*phisubsmall* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="c03b3-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c03b3-111">Typ: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="c03b3-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="c03b3-112">Ein Zeiger auf das Symbol Handle, das auf eine kleine Version eines Symbols verweist.</span><span class="sxs-lookup"><span data-stu-id="c03b3-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="c03b3-113">_phIconLarge \* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="c03b3-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c03b3-114">Typ: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="c03b3-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="c03b3-115">Ein Zeiger auf das Symbol Handle, das auf eine große Version eines Symbols verweist.</span><span class="sxs-lookup"><span data-stu-id="c03b3-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03b3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c03b3-116">Return value</span></span>

<span data-ttu-id="c03b3-117">Typ: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="c03b3-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="c03b3-118">**True** , wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c03b3-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c03b3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c03b3-119">Remarks</span></span>

<span data-ttu-id="c03b3-120">**Mirroricon** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="c03b3-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="c03b3-121">Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 414 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c03b3-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c03b3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c03b3-122">Requirements</span></span>



| <span data-ttu-id="c03b3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c03b3-123">Requirement</span></span> | <span data-ttu-id="c03b3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c03b3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c03b3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c03b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c03b3-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c03b3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="c03b3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c03b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c03b3-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c03b3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c03b3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c03b3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c03b3-130"><dt>Comctl32.dll (Version 5,81 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c03b3-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 


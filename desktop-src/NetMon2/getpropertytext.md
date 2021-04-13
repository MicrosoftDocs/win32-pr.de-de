---
description: Die getpropertytext-Funktion gibt einen Zeiger auf den Eigenschafts Text zurück.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Getpropertytext-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342749"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="1a49e-103">Getpropertytext-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a49e-103">GetPropertyText function</span></span>

<span data-ttu-id="1a49e-104">Die **getpropertytext** -Funktion gibt einen Zeiger auf den Eigenschafts Text zurück.</span><span class="sxs-lookup"><span data-stu-id="1a49e-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a49e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a49e-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="1a49e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a49e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a49e-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a49e-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a49e-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="1a49e-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="1a49e-109">*lppi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a49e-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a49e-110">Zeiger auf eine Eigenschaften Instanz.</span><span class="sxs-lookup"><span data-stu-id="1a49e-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="1a49e-111">*szBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a49e-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a49e-112">Ein Zeiger auf die Zeichenfolge der Eigenschaften Text.</span><span class="sxs-lookup"><span data-stu-id="1a49e-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="1a49e-113">*BufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a49e-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a49e-114">Größe des Textzeichen folgen Puffers.</span><span class="sxs-lookup"><span data-stu-id="1a49e-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a49e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a49e-115">Return value</span></span>

<span data-ttu-id="1a49e-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Eigenschaften Text.</span><span class="sxs-lookup"><span data-stu-id="1a49e-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="1a49e-117">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="1a49e-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a49e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a49e-118">Remarks</span></span>

<span data-ttu-id="1a49e-119">[*Experten*](e.md) und [*Parser*](p.md) können die **getpropertytext** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1a49e-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a49e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a49e-120">Requirements</span></span>



| <span data-ttu-id="1a49e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a49e-121">Requirement</span></span> | <span data-ttu-id="1a49e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1a49e-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1a49e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a49e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a49e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a49e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1a49e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a49e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a49e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a49e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1a49e-127">Header</span><span class="sxs-lookup"><span data-stu-id="1a49e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a49e-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a49e-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1a49e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a49e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a49e-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a49e-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a49e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1a49e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a49e-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a49e-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





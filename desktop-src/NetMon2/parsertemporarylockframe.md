---
description: Die parsertemporarylockframe-Funktion sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn die Funktion den Parser beendet.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Funktion "parametertemporarylockframe" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363338"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="cc191-103">Funktion "parametertemporarylockframe"</span><span class="sxs-lookup"><span data-stu-id="cc191-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="cc191-104">Die **parsertemporarylockframe** -Funktion sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn die Funktion den Parser beendet.</span><span class="sxs-lookup"><span data-stu-id="cc191-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc191-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc191-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="cc191-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc191-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc191-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc191-108">Handle für den Frame, auf den der Parser zeigt.</span><span class="sxs-lookup"><span data-stu-id="cc191-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc191-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc191-109">Return value</span></span>

<span data-ttu-id="cc191-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte der Daten im Frame.</span><span class="sxs-lookup"><span data-stu-id="cc191-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="cc191-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="cc191-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc191-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc191-112">Remarks</span></span>

<span data-ttu-id="cc191-113">Parser sollten die **Lock Frame** -Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc191-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="cc191-114">Wenn ein Parser eine Sperre annimmt und dann einen Fehler generiert oder zurückgibt, ohne den Frame zu entsperren, verlässt der Parser das System in einem Zustand, in dem er keine Protokolle ändern oder Frames Ausschneiden oder kopieren kann.</span><span class="sxs-lookup"><span data-stu-id="cc191-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="cc191-115">Parser sollten die **parsertemporarylockframe** -Funktion verwenden, die eine Sperre nur im Kontext des Funktions Eintrags in den Parser erteilt.</span><span class="sxs-lookup"><span data-stu-id="cc191-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="cc191-116">Beim Beenden des Parsers wird die Sperre für diesen Frame freigegeben.</span><span class="sxs-lookup"><span data-stu-id="cc191-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="cc191-117">Folglich ist der Zeiger nur dann gültig, wenn der Parser vom Aufrufen der **attachproperties** -Funktion oder der **erkenzeframe** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc191-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc191-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc191-118">Requirements</span></span>



| <span data-ttu-id="cc191-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc191-119">Requirement</span></span> | <span data-ttu-id="cc191-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cc191-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc191-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc191-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc191-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc191-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc191-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc191-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc191-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc191-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cc191-125">Header</span><span class="sxs-lookup"><span data-stu-id="cc191-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc191-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc191-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cc191-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc191-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc191-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc191-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc191-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cc191-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc191-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc191-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





---
description: Die getframerecognizedata-Funktion gibt eine Tabelle mit erkenzedata-Strukturen zurück. Jede dieser Strukturen enthält einen Protokoll Bezeichner und einen Offset, der auf den Anfang des angegebenen Protokolls in den Daten zeigt.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Getframerecognizedata-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958715"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="051bc-104">Getframerecognizedata-Funktion</span><span class="sxs-lookup"><span data-stu-id="051bc-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="051bc-105">Die **getframerecognizedata** -Funktion gibt eine Tabelle mit **erkenzedata** -Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="051bc-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="051bc-106">Jede dieser Strukturen enthält einen Protokoll Bezeichner und einen Offset, der auf den Anfang des angegebenen Protokolls in den Daten zeigt.</span><span class="sxs-lookup"><span data-stu-id="051bc-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="051bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="051bc-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="051bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="051bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="051bc-109">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="051bc-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="051bc-110">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="051bc-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="051bc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="051bc-111">Return value</span></span>

<span data-ttu-id="051bc-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine **erkenzedatabel** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="051bc-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="051bc-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="051bc-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="051bc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="051bc-114">Remarks</span></span>

<span data-ttu-id="051bc-115">[*Experten*](e.md) und [*Parser*](p.md) können die **getframerecognizedata** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="051bc-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="051bc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="051bc-116">Requirements</span></span>



| <span data-ttu-id="051bc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="051bc-117">Requirement</span></span> | <span data-ttu-id="051bc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="051bc-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="051bc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="051bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="051bc-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="051bc-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="051bc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="051bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="051bc-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="051bc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="051bc-123">Header</span><span class="sxs-lookup"><span data-stu-id="051bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="051bc-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="051bc-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="051bc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="051bc-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="051bc-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="051bc-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="051bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="051bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="051bc-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="051bc-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





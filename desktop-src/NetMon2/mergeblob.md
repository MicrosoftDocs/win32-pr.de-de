---
description: Die mergeblob-Funktion kopiert alle Einträge aus dem Quell-BLOB in ein Ziel-BLOB.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Mergeblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959020"
---
# <a name="mergeblob-function"></a><span data-ttu-id="08611-103">Mergeblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="08611-103">MergeBlob function</span></span>

<span data-ttu-id="08611-104">Die **mergeblob** -Funktion kopiert alle Einträge aus dem Quell-BLOB in ein Ziel-BLOB.</span><span class="sxs-lookup"><span data-stu-id="08611-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="08611-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08611-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="08611-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08611-107">*hdstblob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="08611-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08611-108">Handle für das Ziel-BLOB.</span><span class="sxs-lookup"><span data-stu-id="08611-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="08611-109">Bei der Eingabe enthält dieses BLOB seine ursprünglichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="08611-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="08611-110">Bei der Ausgabe enthält dieses BLOB seine ursprünglichen Informationen sowie alle Informationen des Quell-BLOBs.</span><span class="sxs-lookup"><span data-stu-id="08611-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="08611-111">*hsrcblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08611-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08611-112">Handle für das Quell-BLOB.</span><span class="sxs-lookup"><span data-stu-id="08611-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08611-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08611-113">Return value</span></span>

<span data-ttu-id="08611-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="08611-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="08611-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="08611-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="08611-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08611-116">Remarks</span></span>

<span data-ttu-id="08611-117">Einträge, die den Quell-und Zieldateien gemeinsam sind, werden mit Daten aus dem Quell-BLOB überschrieben.</span><span class="sxs-lookup"><span data-stu-id="08611-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="08611-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08611-118">Requirements</span></span>



| <span data-ttu-id="08611-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08611-119">Requirement</span></span> | <span data-ttu-id="08611-120">Wert</span><span class="sxs-lookup"><span data-stu-id="08611-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08611-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08611-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08611-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08611-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08611-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08611-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08611-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08611-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08611-125">Header</span><span class="sxs-lookup"><span data-stu-id="08611-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08611-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08611-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="08611-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08611-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="08611-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08611-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="08611-129">DLL</span><span class="sxs-lookup"><span data-stu-id="08611-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08611-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08611-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 





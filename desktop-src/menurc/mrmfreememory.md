---
title: Mrmfrememory-Funktion (mrmresourceindexer. h)
description: Gibt Arbeitsspeicher frei, der von mrmkreateconfiginmemory, mrmkreateresourcefileinmemory, mrmdumpprifileinmemory und mrmdumppridatainmemory zugeordnet wird.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Funktionen von mrmfrememory-Funktionen und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339364"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="b6c25-104">Mrmfrememory-Funktion</span><span class="sxs-lookup"><span data-stu-id="b6c25-104">MrmFreeMemory function</span></span>

<span data-ttu-id="b6c25-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b6c25-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b6c25-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b6c25-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b6c25-107">Gibt Arbeitsspeicher frei, der von [**mrmkreateconfiginmemory**](mrmcreateconfiginmemory.md), [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md), [**mrmdumpprifileinmemory**](mrmdumpprifileinmemory.md)und [**mrmdumppridatainmemory**](mrmdumppridatainmemory.md)zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="b6c25-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="b6c25-108">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b6c25-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c25-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6c25-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="b6c25-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6c25-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c25-111">*Daten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6c25-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c25-112">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="b6c25-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="b6c25-113">Ein Zeiger auf den Arbeitsspeicher, der [von *_ mrmkreateconfiginmemory* \*](mrmcreateconfiginmemory.md), [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md), [**mrmdumpprifileinmemory**](mrmdumpprifileinmemory.md)oder [**mrmdumppridatainmemory**](mrmdumppridatainmemory.md)zugeordnet und zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b6c25-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c25-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6c25-114">Return value</span></span>

<span data-ttu-id="b6c25-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b6c25-115">Type: **HRESULT**</span></span>

<span data-ttu-id="b6c25-116">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="b6c25-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b6c25-117">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b6c25-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c25-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6c25-118">Requirements</span></span>



| <span data-ttu-id="b6c25-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6c25-119">Requirement</span></span> | <span data-ttu-id="b6c25-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b6c25-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c25-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6c25-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c25-122">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6c25-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b6c25-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6c25-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c25-124">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6c25-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b6c25-125">Header</span><span class="sxs-lookup"><span data-stu-id="b6c25-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6c25-126"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c25-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b6c25-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b6c25-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6c25-128"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6c25-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b6c25-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c25-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c25-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6c25-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b6c25-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6c25-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c25-132">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="b6c25-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


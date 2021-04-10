---
title: Mrmdestroyindexerandmessages-Funktion (mrmresourcindexer. h)
description: Gibt Computerressourcen frei, die einem ressourcenindexer zugeordnet sind.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Mrmdestroyindexerandmessages-Funktions Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040981"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="5fb31-104">Mrmdestroyindexerandmessages-Funktion</span><span class="sxs-lookup"><span data-stu-id="5fb31-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="5fb31-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="5fb31-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5fb31-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="5fb31-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5fb31-107">Gibt Computerressourcen frei, die einem ressourcenindexer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5fb31-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="5fb31-108">Zerstört das Handle, gibt den Indexer frei und löscht alle Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="5fb31-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="5fb31-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5fb31-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb31-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fb31-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="5fb31-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fb31-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb31-112">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fb31-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb31-113">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="5fb31-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="5fb31-114">Ein Handle, das den zu löschenden ressourcenindexer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5fb31-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb31-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fb31-115">Return value</span></span>

<span data-ttu-id="5fb31-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5fb31-116">Type: **HRESULT**</span></span>

<span data-ttu-id="5fb31-117">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="5fb31-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="5fb31-118">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5fb31-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb31-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fb31-119">Requirements</span></span>



| <span data-ttu-id="5fb31-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fb31-120">Requirement</span></span> | <span data-ttu-id="5fb31-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb31-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb31-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fb31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fb31-123">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fb31-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5fb31-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fb31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fb31-125">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fb31-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5fb31-126">Header</span><span class="sxs-lookup"><span data-stu-id="5fb31-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fb31-127"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fb31-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="5fb31-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5fb31-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fb31-129"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fb31-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="5fb31-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5fb31-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fb31-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fb31-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5fb31-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb31-133">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="5fb31-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


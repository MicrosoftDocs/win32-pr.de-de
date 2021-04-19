---
title: Wer-Fehler Codes (werapi. h)
description: Die folgende Tabelle enthält eine Liste mit benutzerdefinierten Fehlercodes, die von Windows-Fehlerberichterstattung verwendet werden.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341379"
---
# <a name="wer-error-codes"></a><span data-ttu-id="71b07-103">Wer-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="71b07-103">WER Error Codes</span></span>

<span data-ttu-id="71b07-104">Die folgende Tabelle enthält eine Liste mit benutzerdefinierten Fehlercodes, die von Windows-Fehlerberichterstattung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71b07-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="71b07-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="71b07-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="71b07-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71b07-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="71b07-107"><dt>**\_ \_ nicht genügend \_ Puffer**</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="71b07-108">Ein Puffer ist zu klein, um die Daten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="71b07-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="71b07-109"><dt>**\_ \_ ungültiger \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="71b07-110">Eine Funktion wurde in einer nicht unterstützten Weise aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="71b07-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="71b07-111"><dt>**Länge von wer \_ E \_ \_ überschritten**</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="71b07-112">Eine der Längen Limits wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="71b07-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="71b07-113"><dt>**Wer \_ E \_ fehlt \_ param.**</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="71b07-114">Mindestens ein Parameter fehlt.</span><span class="sxs-lookup"><span data-stu-id="71b07-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="71b07-115"><dt>**Wer \_ E \_ nicht \_ gefunden hat.**</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="71b07-116">Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="71b07-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="71b07-117"><dt>**Wer \_ E \_ Store \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="71b07-118">Der Speicher wurde deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="71b07-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="71b07-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71b07-119">Requirements</span></span>



| <span data-ttu-id="71b07-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71b07-120">Requirement</span></span> | <span data-ttu-id="71b07-121">Wert</span><span class="sxs-lookup"><span data-stu-id="71b07-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="71b07-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71b07-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71b07-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71b07-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="71b07-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71b07-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71b07-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71b07-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="71b07-126">Header</span><span class="sxs-lookup"><span data-stu-id="71b07-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b07-127"><dt>Werapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b07-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 






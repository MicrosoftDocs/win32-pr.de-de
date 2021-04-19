---
UID: ''
title: Guardchecklongjumptarget-Funktion
description: Versucht, zu überprüfen, ob das Ziel eines longjmp gültig ist.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106338653"
---
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="838bb-103">Guardchecklongjumptarget-Funktion</span><span class="sxs-lookup"><span data-stu-id="838bb-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="838bb-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="838bb-104">Description</span></span>

<span data-ttu-id="838bb-105">Versucht, zu überprüfen, ob das Ziel eines [longjmp](/cpp/c-runtime-library/reference/longjmp) für einen Prozess gültig ist, für den [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="838bb-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="838bb-106">Wenn die Zieladresse einer Bild Zuordnung entspricht, werden die gültigen Ziele für die Binärdatei extrahiert.</span><span class="sxs-lookup"><span data-stu-id="838bb-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="838bb-107">Die-Funktion verwendet diese Ziele, um das Ziel zu validieren.</span><span class="sxs-lookup"><span data-stu-id="838bb-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="838bb-108">Wenn die Binärdatei keine Metadaten enthält, mit denen der Satz gültiger *longjmp* -Ziele beschrieben wird, gibt die Funktion **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="838bb-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="838bb-109">Wenn die Zieladresse einer Zuordnung ohne Image entspricht, wie in JIT-Code, wird eine globale schreibgeschützte Richtlinie mit einer globalen schreibgeschützten Richtlinie abgefragt, um zu bestimmen, ob der Sprung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="838bb-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="838bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="838bb-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="838bb-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="838bb-111">TargetAddress [in]</span></span>

<span data-ttu-id="838bb-112">Die Zieladresse für den Sprung.</span><span class="sxs-lookup"><span data-stu-id="838bb-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="838bb-113">Flags [in]</span><span class="sxs-lookup"><span data-stu-id="838bb-113">Flags [in]</span></span>

<span data-ttu-id="838bb-114">Flags, die den Vorgang beschreiben, der für die Adresse ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="838bb-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="838bb-115">Wenn Sie **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1) angeben, beendet diese Funktion den Prozess nicht, wenn das Ziel ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="838bb-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="838bb-116">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="838bb-116">Returns</span></span>

<span data-ttu-id="838bb-117">**True** , wenn das Ziel gültig ist, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="838bb-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="838bb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="838bb-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="838bb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="838bb-119">See also</span></span>

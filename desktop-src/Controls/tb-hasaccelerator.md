---
title: TB_HASACCELERATOR Meldung (kommstrg. h)
description: Ruft die Anzahl der Symbolleisten Schaltflächen ab, die über das angegebene Zugriffstasten Zeichen verfügen.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- Windows-Steuerelemente für TB_HASACCELERATOR Meldung
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477103"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="cea8e-104">TB- \_ hasaccelerator-Meldung</span><span class="sxs-lookup"><span data-stu-id="cea8e-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="cea8e-105">\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="cea8e-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="cea8e-106">Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="cea8e-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="cea8e-107">Ruft die Anzahl der Symbolleisten Schaltflächen ab, die über das angegebene Zugriffstasten Zeichen verfügen.</span><span class="sxs-lookup"><span data-stu-id="cea8e-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="cea8e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cea8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea8e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cea8e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cea8e-110">Ein **WCHAR** , das das zu überprüfende Eingabe Beschleunigungs Zeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="cea8e-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="cea8e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cea8e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cea8e-112">Ein Zeiger auf einen **int** -Wert, der die Anzahl der Schaltflächen mit dem Zugriffstasten-Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="cea8e-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea8e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cea8e-113">Return value</span></span>

<span data-ttu-id="cea8e-114">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea8e-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="cea8e-115">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cea8e-115">Security Considerations</span></span>

<span data-ttu-id="cea8e-116">Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="cea8e-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea8e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cea8e-117">Remarks</span></span>

<span data-ttu-id="cea8e-118">Zuerst fragt das System alle Symbolleisten Schaltflächen für übereinstimmende Acceleratoren ab.</span><span class="sxs-lookup"><span data-stu-id="cea8e-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="cea8e-119">Wenn keine Übereinstimmungen gefunden werden, sendet das System die [TBN \_ mapaccelerator](tbn-mapaccelerator.md) -Benachrichtigung an das übergeordnete Fenster und fordert den Index der Schaltfläche an, die über das angegebene Zugriffstasten Zeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="cea8e-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="cea8e-120">Wenn das übergeordnete Element einen Index bereitstellt, wird die Anzahl auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cea8e-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea8e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cea8e-121">Requirements</span></span>



| <span data-ttu-id="cea8e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cea8e-122">Requirement</span></span> | <span data-ttu-id="cea8e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cea8e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cea8e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cea8e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cea8e-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea8e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cea8e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cea8e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cea8e-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea8e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cea8e-128">Header</span><span class="sxs-lookup"><span data-stu-id="cea8e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea8e-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea8e-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: EM_GETTABLEPARMS Meldung (RichEdit. h)
description: Ruft die Tabellen Parameter für eine Tabellenzeile und die Zellen Parameter für die angegebene Anzahl von Zellen ab.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- Windows-Steuerelemente für EM_GETTABLEPARMS Meldung
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858849"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="e5bc4-104">EM \_ gettableparamems-Meldung</span><span class="sxs-lookup"><span data-stu-id="e5bc4-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="e5bc4-105">Ruft die Tabellen Parameter für eine Tabellenzeile und die Zellen Parameter für die angegebene Anzahl von Zellen ab.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="e5bc4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5bc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5bc4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5bc4-108">Ein Zeiger auf eine [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5bc4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5bc4-110">Ein Zeiger auf eine [**tablecellparamems**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5bc4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5bc4-111">Return value</span></span>

<span data-ttu-id="e5bc4-112">Gibt \_ bei Erfolg S OK oder einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="e5bc4-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e5bc4-113">Return code</span></span>                                                                                    | <span data-ttu-id="e5bc4-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5bc4-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5bc4-115"><dt>**E \_** Fehler</dt></span><span class="sxs-lookup"><span data-stu-id="e5bc4-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="e5bc4-116">Es können keine Änderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-116">Changes cannot be made.</span></span> <span data-ttu-id="e5bc4-117">Dies kann vorkommen, wenn es sich bei dem Steuerelement um ein nur-Text-oder einzeilige Steuerelement handelt oder wenn sich die Einfügemarke in einem mathematischen Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="e5bc4-118">Es tritt auch auf, wenn Tabellen deaktiviert werden, wenn die " [**EM \_ seteditstyleex**](em-seteditstyleex.md) "-Meldung den Wert " **SES \_ Ex \_** relevante" festlegt.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="e5bc4-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e5bc4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="e5bc4-120">Der *wParam* -oder *LPARAM* -Wert ist NULL oder zeigt auf eine ungültige Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="e5bc4-121">Der **cbrow** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur muss gleich `sizeof(TABLEROWPARMS)` oder sizeof (tablerowparamems) 2 \* sizeof (Long) sein.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="e5bc4-122">Der letztere Wert ist die Größe der RichEdit 4,1 **tablerowparamems** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="e5bc4-123">Der **cbcell** -Member der **tablerowparamems** -Struktur muss gleich sein `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="e5bc4-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="e5bc4-124">Die Position des abfragezeichens muss ein Tabellenzeilen Trennzeichen sein.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="e5bc4-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e5bc4-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="e5bc4-126">Es ist nicht genügend Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="e5bc4-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5bc4-127">Remarks</span></span>

<span data-ttu-id="e5bc4-128">Diese Nachricht Ruft die Tabellen Parameter für die Zeile an der Zeichenposition ab, die vom **cpstartrow** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur angegeben wird, sowie die Anzahl der Zellen, die durch den **ccells** -Member der [**tablecellparamems**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="e5bc4-129">Die Zeichenposition, die vom **cpstartrow** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur angegeben wird, muss sich am Anfang der Tabellenzeile oder am endtrennzeichen der Tabellenzeile befinden.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="e5bc4-130">Wenn **cpstartrow** auf 1 festgelegt ist, wird die Zeichenposition von der aktuellen Auswahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="e5bc4-131">Positionieren Sie in diesem Fall die Auswahl am Ende der Zeile (zwischen der Zelle und dem endtrennzeichen der Tabellenzeile), oder wählen Sie die Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5bc4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5bc4-132">Requirements</span></span>



| <span data-ttu-id="e5bc4-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5bc4-133">Requirement</span></span> | <span data-ttu-id="e5bc4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e5bc4-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5bc4-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5bc4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e5bc4-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5bc4-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e5bc4-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5bc4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e5bc4-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5bc4-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5bc4-139">Header</span><span class="sxs-lookup"><span data-stu-id="e5bc4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5bc4-140"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5bc4-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5bc4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5bc4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5bc4-142">**EM \_ settableparamems**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 






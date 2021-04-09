---
title: EM_SETTABLEPARMS Meldung (RichEdit. h)
description: Ändert die Parameter von Zeilen in einer Tabelle.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Windows-Steuerelemente für EM_SETTABLEPARMS Meldung
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949709"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="67d8c-104">EM \_ settableparamems-Meldung</span><span class="sxs-lookup"><span data-stu-id="67d8c-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="67d8c-105">Ändert die Parameter von Zeilen in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="67d8c-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="67d8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67d8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67d8c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67d8c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67d8c-108">Ein Zeiger auf eine [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="67d8c-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="67d8c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67d8c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67d8c-110">Ein Zeiger auf eine [**tablecellparamems**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="67d8c-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67d8c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67d8c-111">Return value</span></span>

<span data-ttu-id="67d8c-112">Gibt \_ bei Erfolg S OK oder einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="67d8c-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="67d8c-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="67d8c-113">Return code</span></span>                                                                                    | <span data-ttu-id="67d8c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67d8c-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67d8c-115"><dt>**E \_** Fehler</dt></span><span class="sxs-lookup"><span data-stu-id="67d8c-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="67d8c-116">Es können keine Änderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="67d8c-116">Changes cannot be made.</span></span> <span data-ttu-id="67d8c-117">Dies kann vorkommen, wenn es sich bei dem Steuerelement um ein nur-Text-oder einzeilige Steuerelement handelt oder wenn sich die Einfügemarke in einem mathematischen Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="67d8c-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="67d8c-118">Sie tritt auch auf, wenn Tabellen deaktiviert sind, oder, wenn die Nachricht " [**EM \_ seteditstyleex**](em-seteditstyleex.md) " den Wert " **SES \_ Ex \_** relevante Werte" festlegt.</span><span class="sxs-lookup"><span data-stu-id="67d8c-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="67d8c-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="67d8c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="67d8c-120">Der *wParam* -oder *LPARAM* -Wert ist NULL oder zeigt auf eine ungültige Struktur.</span><span class="sxs-lookup"><span data-stu-id="67d8c-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="67d8c-121">Der **ccell** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur muss mindestens 1 und nicht größer als 63 sein.</span><span class="sxs-lookup"><span data-stu-id="67d8c-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="67d8c-122">Der **cbrow** -Member muss gleich `sizeof(TABLEROWPARMS)` oder sein `sizeof(TABLEROWPARMS)   2*sizeof(long)` .</span><span class="sxs-lookup"><span data-stu-id="67d8c-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="67d8c-123">Der letztere Wert ist die Größe der RichEdit 4,1 **tablerowparamems** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="67d8c-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="67d8c-124">Der **cbcell** -Member von **tablerowparamems** muss gleich sein `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="67d8c-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="67d8c-125">Die Einfügemarke muss sich am Anfang einer Tabelle oder innerhalb einer Tabellenzeile befinden, und die Anzahl der Zellen kann nur um eins geändert werden.</span><span class="sxs-lookup"><span data-stu-id="67d8c-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="67d8c-126"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="67d8c-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="67d8c-127">Es ist nicht genügend Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67d8c-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="67d8c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67d8c-128">Remarks</span></span>

<span data-ttu-id="67d8c-129">Diese Meldung ändert die Parameter der Anzahl von Zeilen, die durch das **cRow** -Element der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur angegeben werden, wenn die Tabelle viele aufeinander folgende Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="67d8c-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="67d8c-130">Wenn der Wert für " **cRow** " kleiner als 0 ist, wird die Meldung bis zum Ende der Tabelle durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="67d8c-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="67d8c-131">Wenn die Anzahl der neuen Zellen von der Anzahl der aktuellen Zellen um + 1 oder 1 abweicht, wird die Zelle an dem Index eingefügt oder gelöscht, der durch den **icell** -Member von **tablerowparamems** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67d8c-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="67d8c-132">Die Zeile der Anfangs Tabelle wird durch eine Zeichenposition identifiziert.</span><span class="sxs-lookup"><span data-stu-id="67d8c-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="67d8c-133">Diese Position wird von **cpstartrow** -Membern mit Werten angegeben, die größer oder gleich 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="67d8c-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="67d8c-134">Die Position sollte sich in der Tabellenzeile befinden, jedoch nicht innerhalb einer geschachtelten Tabelle, es sei denn, Sie möchten die Parameter der Tabelle ändern.</span><span class="sxs-lookup"><span data-stu-id="67d8c-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="67d8c-135">Wenn der **cpstartrow** -Member 1 ist, wird die Zeichenposition von der aktuellen Auswahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="67d8c-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="67d8c-136">Positionieren Sie hierfür die Auswahl an einer beliebigen Position innerhalb der Tabellenzeile, oder wählen Sie die Zeile mit dem aktiven Ende der Auswahl am Ende der Tabellenzeile aus.</span><span class="sxs-lookup"><span data-stu-id="67d8c-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d8c-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67d8c-137">Requirements</span></span>



| <span data-ttu-id="67d8c-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67d8c-138">Requirement</span></span> | <span data-ttu-id="67d8c-139">Wert</span><span class="sxs-lookup"><span data-stu-id="67d8c-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67d8c-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67d8c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="67d8c-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67d8c-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="67d8c-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67d8c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="67d8c-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67d8c-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67d8c-144">Header</span><span class="sxs-lookup"><span data-stu-id="67d8c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="67d8c-145"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d8c-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d8c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67d8c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d8c-147">**EM \_ gettablesparms**</span><span class="sxs-lookup"><span data-stu-id="67d8c-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 






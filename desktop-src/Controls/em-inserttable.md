---
title: EM_INSERTTABLE Meldung (RichEdit. h)
description: Fügt eine oder mehrere identische Tabellenzeilen mit leeren Zellen ein.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- Windows-Steuerelemente für EM_INSERTTABLE Meldung
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475555"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="258f9-104">EM \_ insertfähige Nachricht</span><span class="sxs-lookup"><span data-stu-id="258f9-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="258f9-105">Fügt eine oder mehrere identische Tabellenzeilen mit leeren Zellen ein.</span><span class="sxs-lookup"><span data-stu-id="258f9-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="258f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="258f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="258f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="258f9-108">Ein Zeiger auf eine [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="258f9-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="258f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="258f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="258f9-110">Ein Zeiger auf eine [**tablecellparamems**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="258f9-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258f9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="258f9-111">Return value</span></span>

<span data-ttu-id="258f9-112">Gibt S \_ OK zurück, wenn die Tabelle eingefügt wird, andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="258f9-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="258f9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="258f9-113">Remarks</span></span>

<span data-ttu-id="258f9-114">Wenn der **cpstartrow** -Member von [**tablerowparms**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) 1 ist, löscht diese Meldung den markierten Text (sofern vorhanden) und fügt dann leere Tabellenzeilen mit den Zeilen-und Zell Parametern ein, die von *wParam* und *LPARAM* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="258f9-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="258f9-115">Dadurch wird die Auswahl auf den Anfang der ersten Zelle in der ersten Zeile verwiesen.</span><span class="sxs-lookup"><span data-stu-id="258f9-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="258f9-116">Der Client kann dann die Tabellenzellen auffüllen, indem er die Auswahl (oder ein [**itextrange**](/windows/desktop/api/Tom/nn-tom-itextrange)) auf die verschiedenen Zell Endmarkierungen zeigt und den gewünschten Text einfügt und formatiert.</span><span class="sxs-lookup"><span data-stu-id="258f9-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="258f9-117">Dieser Text kann Zeilen in der Zeilen Tabelle einschließen.</span><span class="sxs-lookup"><span data-stu-id="258f9-117">Such text can include nested table rows.</span></span> <span data-ttu-id="258f9-118">Wenn der **cpstartrow** -Member der **tablerowparamems** gleich 0 (null) oder größer ist, werden die Tabellenzeilen an der von **cpstartrow** angegebenen Zeichenposition eingefügt.</span><span class="sxs-lookup"><span data-stu-id="258f9-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="258f9-119">Dadurch wird nur die aktuelle Auswahl geändert, wenn die Tabelle in den ausgewählten Text eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="258f9-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="258f9-120">Eine Microsoft Rich Edit-Tabelle besteht aus einer Sequenz von Tabellenzeilen, die wiederum aus Sequenzen von Absätzen bestehen.</span><span class="sxs-lookup"><span data-stu-id="258f9-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="258f9-121">Eine Tabellenzeile beginnt mit dem speziellen Trennzeichen Absatz für zwei Zeichen u + FFF9 u + 000D und endet mit dem zweistelligen Trennzeichen Absatz u + fffb u + 000D.</span><span class="sxs-lookup"><span data-stu-id="258f9-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="258f9-122">Jede Zelle wird von der Zelle u + 0007 beendet, die als eine feste Zeichenfolge gekennzeichnet wird, ebenso wie U + 000D (CR).</span><span class="sxs-lookup"><span data-stu-id="258f9-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="258f9-123">Die Tabellenzeilen-und Zellen Parameter werden als spezielle Absatz Formatierung der Tabellenzeilen Trennzeichen behandelt.</span><span class="sxs-lookup"><span data-stu-id="258f9-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="258f9-124">Die Formatierung enthält die Informationen in der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="258f9-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="258f9-125">Die Zellen Parameter, die von der [**tablecellparms**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur angegeben werden, werden in einer erweiterten Version des Registerkarten Arrays gespeichert.</span><span class="sxs-lookup"><span data-stu-id="258f9-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="258f9-126">In diesem Format können Tabellen in anderen Tabellen geschachtelt werden, bis zu 15 Ebenen tief.</span><span class="sxs-lookup"><span data-stu-id="258f9-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="258f9-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="258f9-127">Requirements</span></span>



| <span data-ttu-id="258f9-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="258f9-128">Requirement</span></span> | <span data-ttu-id="258f9-129">Wert</span><span class="sxs-lookup"><span data-stu-id="258f9-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="258f9-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="258f9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="258f9-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="258f9-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="258f9-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="258f9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="258f9-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="258f9-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="258f9-134">Header</span><span class="sxs-lookup"><span data-stu-id="258f9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="258f9-135"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="258f9-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="258f9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="258f9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258f9-137">**EM \_ InsertImage**</span><span class="sxs-lookup"><span data-stu-id="258f9-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 






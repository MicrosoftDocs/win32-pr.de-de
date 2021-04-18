---
title: TB_ADDSTRING Meldung (kommstrg. h)
description: Fügt eine neue Zeichenfolge zum Zeichen folgen Pool der Symbolleiste hinzu.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Windows-Steuerelemente für TB_ADDSTRING Meldung
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345344"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="f3669-104">TB \_ AddString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f3669-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="f3669-105">Fügt eine neue Zeichenfolge zum Zeichen folgen Pool der Symbolleiste hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3669-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3669-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3669-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3669-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3669-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3669-108">Handle für die Modul Instanz mit einer ausführbaren Datei, die die Zeichen folgen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f3669-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="f3669-109">Wenn *LPARAM* stattdessen auf ein Zeichen Array mit einer oder mehreren Zeichen folgen verweist, legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="f3669-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3669-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3669-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3669-111">Der Ressourcen Bezeichner für die Zeichen folgen Ressource oder ein Zeiger auf ein TCHAR-Array.</span><span class="sxs-lookup"><span data-stu-id="f3669-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="f3669-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f3669-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3669-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3669-113">Return value</span></span>

<span data-ttu-id="f3669-114">Gibt den Index der ersten neuen Zeichenfolge zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="f3669-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3669-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3669-115">Remarks</span></span>

<span data-ttu-id="f3669-116">Wenn *wParam* den Wert **null** hat, verweist *LPARAM* auf ein Zeichen Array mit einer oder mehreren null-terminierten Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="f3669-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="f3669-117">Die letzte Zeichenfolge im Array muss mit zwei NULL-Zeichen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3669-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="f3669-118">Wenn *wParam* die HINSTANCE der Anwendung oder eines anderen Moduls mit einer Zeichen folgen Ressource ist, ist *LPARAM* der Ressourcen Bezeichner der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f3669-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="f3669-119">Jedes Element in der Zeichenfolge muss mit einem beliebigen Trennzeichen beginnen, und die Zeichenfolge muss mit zwei Zeichen enden Zeichen enden.</span><span class="sxs-lookup"><span data-stu-id="f3669-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="f3669-120">Beispielsweise kann der Text für drei Schaltflächen in der Zeichen folgen Tabelle als "/New/Open/Save//" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3669-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="f3669-121">Die Meldung gibt den Index "New" im Zeichen folgen Pool der Symbolleiste zurück, und die anderen Elemente befinden sich in aufeinander folgenden Positionen.</span><span class="sxs-lookup"><span data-stu-id="f3669-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3669-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3669-122">Requirements</span></span>



| <span data-ttu-id="f3669-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3669-123">Requirement</span></span> | <span data-ttu-id="f3669-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f3669-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3669-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3669-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3669-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3669-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3669-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3669-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3669-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3669-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3669-129">Header</span><span class="sxs-lookup"><span data-stu-id="f3669-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3669-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3669-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f3669-131">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f3669-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f3669-132">**TB \_ Addstringw** (Unicode) und **TB \_ addstraninga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f3669-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 






---
title: Class-Anweisung
description: Definiert die Klasse des Dialog Felds.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Klassen Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948674"
---
# <a name="class-statement"></a><span data-ttu-id="2abc9-104">Class-Anweisung</span><span class="sxs-lookup"><span data-stu-id="2abc9-104">CLASS statement</span></span>

<span data-ttu-id="2abc9-105">Definiert die Klasse des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="2abc9-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="2abc9-106">Die **Class** -Anweisung wird im optionalen Abschnitt vor dem Hauptabschnitt der [**Dialog**](dialog-resource.md) Feld Anweisung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2abc9-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="2abc9-107">Wenn keine Klasse angegeben wird, wird die Standard Dialogklasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="2abc9-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="2abc9-108"><span id="class"></span><span id="CLASS"></span>*klassi*</span><span class="sxs-lookup"><span data-stu-id="2abc9-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="2abc9-109">Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die die Klasse des Dialog Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="2abc9-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="2abc9-110">Wenn die Fenster Prozedur für die Klasse keine an Sie gesendete Nachricht verarbeitet, muss Sie die Funktion [**defdlgproc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) aufgerufen werden, um sicherzustellen, dass alle Nachrichten ordnungsgemäß für das Dialogfeld verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2abc9-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="2abc9-111">Eine private Klasse kann **defdlgproc** als Standardfenster Prozedur verwenden.</span><span class="sxs-lookup"><span data-stu-id="2abc9-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="2abc9-112">Die Klasse muss beim **CbWndExtra** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur, die auf **dlgwindowextra** festgelegt ist, registriert werden.</span><span class="sxs-lookup"><span data-stu-id="2abc9-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2abc9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2abc9-113">Remarks</span></span>

<span data-ttu-id="2abc9-114">Die **Class** -Anweisung sollte nur in besonderen Fällen verwendet werden, da Sie die normale Verarbeitung eines Dialog Felds überschreibt.</span><span class="sxs-lookup"><span data-stu-id="2abc9-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="2abc9-115">Die **Class** -Anweisung konvertiert ein Dialogfeld in ein Fenster der angegebenen Klasse. abhängig von der-Klasse kann dies zu unerwünschten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="2abc9-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="2abc9-116">Verwenden Sie die neu definierten Steuerelement Klassennamen nicht mit dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="2abc9-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="2abc9-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2abc9-117">Examples</span></span>

<span data-ttu-id="2abc9-118">Im folgenden Beispiel wird die Verwendung der **Class** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="2abc9-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="2abc9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2abc9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abc9-120">**Defdlgproc**</span><span class="sxs-lookup"><span data-stu-id="2abc9-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="2abc9-121">**Dialog**</span><span class="sxs-lookup"><span data-stu-id="2abc9-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 
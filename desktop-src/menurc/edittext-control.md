---
title: EDITTEXT-Steuerelement
description: Definiert ein Bearbeitungs Steuerelement, das zur Edit-Klasse gehört.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- EDITTEXT-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725880"
---
# <a name="edittext-control"></a><span data-ttu-id="eaf6b-104">EDITTEXT-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="eaf6b-104">EDITTEXT control</span></span>

<span data-ttu-id="eaf6b-105">Definiert ein Bearbeitungs Steuerelement, das zur Edit-Klasse gehört.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="eaf6b-106">Es wird ein rechteckiger Bereich erstellt, in dem der Benutzer Text eingeben und bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="eaf6b-107">Das Steuerelement zeigt einen Cursor an, wenn der Benutzer auf die Maus klickt.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="eaf6b-108">Der Benutzer kann dann die Tastatur verwenden, um Text einzugeben oder den vorhandenen Text zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="eaf6b-109">Zum Bearbeiten von Schlüsseln gehören die Rücktaste und die Schlüssel zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="eaf6b-110">Der Benutzer kann auch mit der Maus Zeichen auswählen, die gelöscht werden sollen, oder den Ort auswählen, an dem neue Zeichen eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="eaf6b-111"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="eaf6b-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="eaf6b-112">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-112">Control styles.</span></span> <span data-ttu-id="eaf6b-113">Bei diesem Wert kann es sich um eine Kombination der Stile der Bearbeitungs Klasse und der folgenden Stile handeln: **WS \_ Tabstopps**, **WS \_ Group**, **WS \_ VScroll**, **WS \_ HScroll** und **WS \_ deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="eaf6b-114">Wenn Sie keinen Stil angeben, ist der Standardstil `ES_LEFT | WS_BORDER | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="eaf6b-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="eaf6b-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eaf6b-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eaf6b-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaf6b-116">Examples</span></span>

<span data-ttu-id="eaf6b-117">Im folgenden Beispiel wird die Verwendung der **EDITTEXT** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="eaf6b-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="eaf6b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaf6b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf6b-119">Steuerelemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="eaf6b-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 
---
title: Style-Anweisung
description: Definiert den Fenster Stil des Dialog Felds. Der Fenster Stil gibt an, ob das Feld ein Popup-oder ein untergeordnetes Fenster ist.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Stil Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390256"
---
# <a name="style-statement"></a><span data-ttu-id="70a30-105">Style-Anweisung</span><span class="sxs-lookup"><span data-stu-id="70a30-105">STYLE statement</span></span>

<span data-ttu-id="70a30-106">Definiert den Fenster Stil des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="70a30-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="70a30-107">Der Fenster Stil gibt an, ob das Feld ein Popup-oder ein untergeordnetes Fenster ist.</span><span class="sxs-lookup"><span data-stu-id="70a30-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="70a30-108"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="70a30-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="70a30-109">Der Fensterstil.</span><span class="sxs-lookup"><span data-stu-id="70a30-109">The window style.</span></span> <span data-ttu-id="70a30-110">Dieser Parameter kann ein ganzzahliger Wert oder eine Kombination aus Fenster Stil Werten (z. b. **WS \_ Caption** und **WS \_ sysmenu**) und Dialogfeld-Stil Werten (z. b. **DS \_ Center**) sein.</span><span class="sxs-lookup"><span data-stu-id="70a30-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="70a30-111">Eine Liste der Fenster Stile finden Sie unter [Fenster Stile](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="70a30-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="70a30-112">Eine Liste der Dialogfeld Stile finden Sie unter [Dialogfeld Vorlagen Stile](../dlgbox/about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="70a30-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="70a30-113">Wenn Sie die Werte für das Fenster oder den Dialogfeld Stil verwenden, müssen Sie Windows. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="70a30-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 
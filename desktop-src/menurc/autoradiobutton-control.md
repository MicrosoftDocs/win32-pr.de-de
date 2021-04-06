---
title: AUTORADIOBUTTON-Steuerelement
description: Definiert ein automatisches Optionsfeld-Steuerelement. Dieses Steuerelement führt den gegenseitigen Ausschluss mit den anderen AUTORADIOBUTTON-Steuerelementen in derselben Gruppe automatisch aus. Wenn die Schaltfläche ausgewählt wird, wird die Anwendung mit dem \_ angeklickten BN benachrichtigt.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- AUTORADIOBUTTON-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718353"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="d6613-106">AUTORADIOBUTTON-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d6613-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="d6613-107">Definiert ein automatisches Optionsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d6613-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="d6613-108">Dieses Steuerelement führt den gegenseitigen Ausschluss mit den anderen **AUTORADIOBUTTON** -Steuerelementen in derselben Gruppe automatisch aus.</span><span class="sxs-lookup"><span data-stu-id="d6613-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="d6613-109">Wenn die Schaltfläche ausgewählt wird, wird die Anwendung mit **dem \_ angeklickten BN** benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d6613-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="d6613-110"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="d6613-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="d6613-111">Text, der neben dem Optionsfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6613-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="d6613-112"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="d6613-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="d6613-113">Stile für das Optionsfeld automatisch, bei dem es sich um eine Kombination aus Schaltflächen Klassen Formaten und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ Deaktivierte** und **WS- \_ Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="d6613-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="d6613-114">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTORADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="d6613-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="d6613-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6613-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d6613-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6613-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6613-117">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="d6613-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="d6613-118">Options Felder</span><span class="sxs-lookup"><span data-stu-id="d6613-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="d6613-119">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="d6613-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 





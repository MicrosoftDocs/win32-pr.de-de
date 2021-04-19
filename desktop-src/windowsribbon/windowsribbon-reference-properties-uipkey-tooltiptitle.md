---
title: UI_PKEY_TooltipTitle
description: Bezeichnet die Benutzeroberflächen- \_ pkey- \_ ToolTipTitle-Eigenschaft.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341469"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="6a86b-103">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="6a86b-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="6a86b-104">Bezeichnet die Benutzeroberflächen- \_ pkey- \_ ToolTipTitle-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6a86b-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="6a86b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a86b-105">Remarks</span></span>

<span data-ttu-id="6a86b-106">\_Der UI pkey \_ -ToolTipTitle wird von einer Anwendung verwendet, um die QuickInfo von Registerkarten, Gruppen, Schaltflächen, Galerie Elementen und anderen Menü Band Steuerelementen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6a86b-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="6a86b-107">Der Eigenschafts Wert ist eine Zeichenfolge, die auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6a86b-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="6a86b-108">Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6a86b-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="6a86b-109">Die Rechte Ausrichtung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a86b-109">Right alignment is not supported.</span></span>

<span data-ttu-id="6a86b-110">Die maximale Länge des UI- \_ pkey- \_ ToolTipTitle ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="6a86b-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="6a86b-111">Um ein kaufmännisches und-Zeichen in einer QuickInfo anzuzeigen, versehen Sie die Bezeichnung für Sonderzeichen mit einem doppelten kaufmännisches und-Zeichen ( `&&` ), wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a86b-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="6a86b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a86b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a86b-113">Ressourcen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a86b-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="6a86b-114">**Command. ToolTipTitle**</span><span class="sxs-lookup"><span data-stu-id="6a86b-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="6a86b-115">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="6a86b-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





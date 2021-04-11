---
title: Das Sprechblasen Objekt
description: Das Sprechblasen Objekt
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208889"
---
# <a name="the-balloon-object"></a><span data-ttu-id="3efe1-103">Das Sprechblasen Objekt</span><span class="sxs-lookup"><span data-stu-id="3efe1-103">The Balloon Object</span></span>

<span data-ttu-id="3efe1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3efe1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3efe1-105">Der Microsoft-Agent unterstützt die Text Beschriftungen der Sprech Methode mithilfe einer Wort [**Sprech**](speak-method.md) Blase.</span><span class="sxs-lookup"><span data-stu-id="3efe1-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="3efe1-106">Die Methode " [**Think**](think-method.md) " ermöglicht es Ihnen, Text ohne Audioausgabe in einer "gedachten" Wort Sprechblase anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3efe1-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="3efe1-107">Die Standardwerte für das anfängliche Wort Sprechblasen Fenster eines Zeichens werden im Microsoft-Agent-Zeichen-Editor definiert und kompiliert.</span><span class="sxs-lookup"><span data-stu-id="3efe1-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3efe1-108">Nach der Ausführung werden die [**aktivierten**](enabled-property.md) und [**Schriftart**](https://www.bing.com/search?q=**Font**) Eigenschaften des Sprechblasen möglicherweise vom Benutzer überschrieben.</span><span class="sxs-lookup"><span data-stu-id="3efe1-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="3efe1-109">Wenn ein Benutzer die Eigenschaften der Wort Sprechblase ändert, wirkt sich dies auf alle Zeichen aus.</span><span class="sxs-lookup"><span data-stu-id="3efe1-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="3efe1-110">Sowohl für die Sprech [**-als**](think-method.md) auch für die [**Sprech**](speak-method.md) Blasen Verwendung werden dieselben Eigenschaften Einstellungen wie für die Größe verwendet.</span><span class="sxs-lookup"><span data-stu-id="3efe1-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="3efe1-111">Sie können auf die Eigenschaften für die Wort Sprechblase eines Zeichens über [**das Sprech**](/windows/desktop/lwef/the-balloon-object) Blasen Objekt zugreifen, das ein untergeordnetes Element des [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="3efe1-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="3efe1-112">Das Sprech [**Blasen Objekt unterstützt die folgenden**](/windows/desktop/lwef/the-balloon-object) Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3efe1-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="3efe1-113">**BackColor**</span><span class="sxs-lookup"><span data-stu-id="3efe1-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="3efe1-114">**BorderColor**</span><span class="sxs-lookup"><span data-stu-id="3efe1-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="3efe1-115">**Charsperline**</span><span class="sxs-lookup"><span data-stu-id="3efe1-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="3efe1-116">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="3efe1-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="3efe1-117">**Fontcharset**</span><span class="sxs-lookup"><span data-stu-id="3efe1-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="3efe1-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="3efe1-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="3efe1-119">**SchriftFett**</span><span class="sxs-lookup"><span data-stu-id="3efe1-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="3efe1-120">**FontItalic**</span><span class="sxs-lookup"><span data-stu-id="3efe1-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="3efe1-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="3efe1-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="3efe1-122">**FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="3efe1-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="3efe1-123">**Fontunter Streichung**</span><span class="sxs-lookup"><span data-stu-id="3efe1-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="3efe1-124">**ForeColor**</span><span class="sxs-lookup"><span data-stu-id="3efe1-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="3efe1-125">**Anzahl von Zeilen**</span><span class="sxs-lookup"><span data-stu-id="3efe1-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="3efe1-126">**Stil**</span><span class="sxs-lookup"><span data-stu-id="3efe1-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="3efe1-127">**Sichtbar**</span><span class="sxs-lookup"><span data-stu-id="3efe1-127">**Visible**</span></span>](visible-property-bal.md)

 

 
---
title: Leitfaden für internationale Text-und Schriftarten
description: Leitfaden für internationale Text-und Schriftarten
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390335"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="f3a76-103">Leitfaden für internationale Text-und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="f3a76-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f3a76-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="f3a76-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="f3a76-105">Clients-Windows 8 \| Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3a76-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="f3a76-106">Server-Windows Server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f3a76-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="f3a76-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3a76-107">Description</span></span>

<span data-ttu-id="f3a76-108">Seit Windows 2000 wurde in jeder Hauptversion von Windows eine Textanzeige Unterstützung für neue Skripts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f3a76-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="f3a76-109">Sie finden Beschreibungen der Änderungen, die in den einzelnen Hauptversionen des Artikels [Skript-und Schriftart Unterstützung für Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) im Artikel zum [globalen Entwicklungs Center von Go](https://msdn.microsoft.com/goglobal/default)vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="f3a76-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="f3a76-110">Beachten Sie, dass die Unterstützung für ein Skript bestimmte Änderungen an Text Stapel Komponenten und Änderungen an Schriftarten erfordern kann.</span><span class="sxs-lookup"><span data-stu-id="f3a76-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="f3a76-111">Das Windows-Betriebssystem verfügt über viele Text Stapel Komponenten: DirectWrite, GDI, uniscri, GDI+, WPF, RichEdit, ComCtl32 und andere.</span><span class="sxs-lookup"><span data-stu-id="f3a76-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="f3a76-112">Die bereitgestellten Informationen betreffen hauptsächlich GDI und DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f3a76-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="f3a76-113">Dies gilt auch für Benutzeroberflächen-Frameworks wie RichEdit oder den MSHTML-renderingagent, der für Windows 8 Store-Apps und für das Rendern von Webinhalt verwendet wird, obwohl diese Komponenten möglicherweise bestimmte Unterschiede aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f3a76-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="f3a76-114">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="f3a76-114">Best Practices</span></span>

<span data-ttu-id="f3a76-115">**Typografieanleitung für Entwickler**</span><span class="sxs-lookup"><span data-stu-id="f3a76-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="f3a76-116">Typografie ist der Kern der Microsoft-Entwurfs Sprache.</span><span class="sxs-lookup"><span data-stu-id="f3a76-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="f3a76-117">Jedes der Microsoft-Entwurfs Prinzipien stärkt die Wichtigkeit der Typografie.</span><span class="sxs-lookup"><span data-stu-id="f3a76-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="f3a76-118">Zum ersten Mal verfügen App-Entwickler über eine Reihe von Frameworks, die erweiterte typografische Features unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f3a76-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="f3a76-119">Informationen zur Verwendung von JavaScript und HTML zum Anzeigen und Bearbeiten von Text in Windows Store-Apps finden Sie unter [anzeigen und](/previous-versions/windows/apps/hh465442(v=win.10)) Bearbeiten von Text.</span><span class="sxs-lookup"><span data-stu-id="f3a76-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="f3a76-120">**Schriftmetriken**</span><span class="sxs-lookup"><span data-stu-id="f3a76-120">**Font metrics**</span></span>

<span data-ttu-id="f3a76-121">Die Schriftart Metrik ist ein Bereich, der für Anwendungsentwickler besonders wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="f3a76-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="f3a76-122">Schriftart Dateien enthalten verschiedene Werte im Zusammenhang mit vertikalen und horizontalen Metriken.</span><span class="sxs-lookup"><span data-stu-id="f3a76-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="f3a76-123">Diese Werte sind in der [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/) dokumentiert und sind über eine Vielzahl von APIs verfügbar, die in der [Struktur der dwrite- \_ Schriftart \_ Metriken](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) und in der [TextMetric-Struktur](/windows/win32/api/wingdi/ns-wingdi-textmetrica)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f3a76-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="f3a76-124">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f3a76-124">Resources</span></span>

-   [<span data-ttu-id="f3a76-125">Skript-und Schriftart Unterstützung für Windows</span><span class="sxs-lookup"><span data-stu-id="f3a76-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="f3a76-126">Go Global Development Center</span><span class="sxs-lookup"><span data-stu-id="f3a76-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="f3a76-127">[Anzeigen und Bearbeiten von Text](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f3a76-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="f3a76-128">OpenType-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f3a76-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="f3a76-129">Dwrite- \_ Schriftart \_ metrikstruktur</span><span class="sxs-lookup"><span data-stu-id="f3a76-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="f3a76-130">TextMetric-Struktur</span><span class="sxs-lookup"><span data-stu-id="f3a76-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 
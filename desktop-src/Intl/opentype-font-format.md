---
description: Das Unicode-basierte OpenType-Schriftformat erweitert das TrueType-Schriftart Dateiformat.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: OpenType-Schriftartformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349706"
---
# <a name="opentype-font-format"></a><span data-ttu-id="3f238-103">OpenType-Schriftartformat</span><span class="sxs-lookup"><span data-stu-id="3f238-103">OpenType Font Format</span></span>

<span data-ttu-id="3f238-104">Das Unicode-basierte OpenType-Schriftformat erweitert das TrueType-Schriftart Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="3f238-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="3f238-105">OpenType-Schriftarten ermöglichen die Zuordnung zwischen [Zeichen und Symbolen](uniscribe-glossary.md), die Unterstützung von Ligaturen, Positions Formularen, Alternativen und anderen Substitutionen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3f238-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="3f238-106">OpenType-Schriftarten können auch Informationen enthalten, die eine zweidimensionale Symbol Positionierung und eine Symbol Anlage unterstützen und entweder TrueType-oder PostScript-Gliederungen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="3f238-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="3f238-107">Layoutfunktionen innerhalb von OpenType-Schriftarten werden nach Skripts und Sprachen organisiert, sodass eine einzelne Schriftart mehrere Schreibsysteme unterstützen kann, auch innerhalb desselben Skripts.</span><span class="sxs-lookup"><span data-stu-id="3f238-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="3f238-108">Um die Konsistenz bei textlayoutvorgängen zu gewährleisten und unnötigen mehr Aufwand in Schriftart Dateien oder Anwendungen zu vermeiden, sind viele Text Layout-und sprach Semantik Algorithmen in uniwriter enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f238-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="3f238-109">Dadurch ist es dem Schriftart Entwickler nicht mehr erforderlich, generalisierte Skript Regeln innerhalb einer Schriftart zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3f238-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="3f238-110">Anwendungen können bestimmte Kenntnisse oder Vorlieben in Bezug auf das Skript Layout einbringen.</span><span class="sxs-lookup"><span data-stu-id="3f238-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="3f238-111">OpenType-Layoutschriftarten können sogar Layoutregeln enthalten, die die von den Betriebssystemdiensten angewendeten ersetzen oder ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3f238-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="3f238-112">Durch die geschichtete Struktur von Betriebssystemdiensten, die das Text Layout unterstützen, kann eine Anwendung die zu verwendenden Layoutinformationen auswählen und auswählen, wie Sie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f238-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="3f238-113">Weitere Informationen finden Sie in der [Übersicht über die Microsoft-typografiespezifikationen](https://www.microsoft.com/typography/SpecificationsOverview.mspx) oder die [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/).</span><span class="sxs-lookup"><span data-stu-id="3f238-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f238-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f238-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f238-115">Informationen zu uniscri</span><span class="sxs-lookup"><span data-stu-id="3f238-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 




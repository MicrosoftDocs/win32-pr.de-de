---
description: Das Unicode-basierte OpenType-Schriftformat erweitert das TrueType-Schriftdateiformat.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: OpenType-Schriftartformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18324f3a9c84553da81c9f9723a2ecd67c03539b4dd39c7a80afc4be5cdcda66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147093"
---
# <a name="opentype-font-format"></a>OpenType-Schriftartformat

Das Unicode-basierte OpenType-Schriftformat erweitert das TrueType-Schriftdateiformat. OpenType-Schriftarten ermöglichen die Zuordnung zwischen Zeichen und [Glyphen](uniscribe-glossary.md)und ermöglichen die Unterstützung vonLigaturen, Positionsformen, Alternativen und anderen Ersetzungen. OpenType-Schriftarten können auch Informationen enthalten, die die zweidimensionale Glyphenpositionierung und die Glyphenanlage unterstützen, und entweder TrueType oder PostScript Konturen enthalten.

Layoutfunktionen in OpenType-Schriftarten sind nach Skripts und Sprachen organisiert, sodass eine einzelne Schriftart mehrere Schreibsysteme unterstützen kann, sogar innerhalb desselben Skripts. Um Konsistenz bei Textlayoutvorgängen sicherzustellen und unnötigen Mehraufwand in Schriftartdateien oder Anwendungen zu vermeiden, sind viele der Textlayout- und Sprachsemantikalgorithmen in Uniscribe enthalten. Dadurch muss der Schriftartentwickler keine generalisierten Skriptregeln innerhalb einer Schriftart definieren.

Anwendungen können bestimmte Kenntnisse oder Präferenzen in Bezug auf das Skriptlayout einführen. OpenType-Layoutschriftarten enthalten möglicherweise sogar Layoutregeln, die die von Betriebssystemdiensten angewendeten Regeln duplizieren oder ersetzen. Die mehrstufige Struktur von Betriebssystemdiensten, die das Textlayout unterstützen, ermöglicht es einer Anwendung, die zu verwendende Layoutinformation auszuwählen und auszuwählen, wie sie angewendet werden soll. Weitere Informationen finden Sie in der [Übersicht über die Microsoft-Typografiespezifikationen](https://www.microsoft.com/typography/SpecificationsOverview.mspx) oder in der [OpenType-Spezifikation.](https://www.microsoft.com/typography/otspec/)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 




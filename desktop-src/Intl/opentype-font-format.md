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
# <a name="opentype-font-format"></a>OpenType-Schriftartformat

Das Unicode-basierte OpenType-Schriftformat erweitert das TrueType-Schriftart Dateiformat. OpenType-Schriftarten ermöglichen die Zuordnung zwischen [Zeichen und Symbolen](uniscribe-glossary.md), die Unterstützung von Ligaturen, Positions Formularen, Alternativen und anderen Substitutionen ermöglicht. OpenType-Schriftarten können auch Informationen enthalten, die eine zweidimensionale Symbol Positionierung und eine Symbol Anlage unterstützen und entweder TrueType-oder PostScript-Gliederungen enthalten können.

Layoutfunktionen innerhalb von OpenType-Schriftarten werden nach Skripts und Sprachen organisiert, sodass eine einzelne Schriftart mehrere Schreibsysteme unterstützen kann, auch innerhalb desselben Skripts. Um die Konsistenz bei textlayoutvorgängen zu gewährleisten und unnötigen mehr Aufwand in Schriftart Dateien oder Anwendungen zu vermeiden, sind viele Text Layout-und sprach Semantik Algorithmen in uniwriter enthalten. Dadurch ist es dem Schriftart Entwickler nicht mehr erforderlich, generalisierte Skript Regeln innerhalb einer Schriftart zu definieren.

Anwendungen können bestimmte Kenntnisse oder Vorlieben in Bezug auf das Skript Layout einbringen. OpenType-Layoutschriftarten können sogar Layoutregeln enthalten, die die von den Betriebssystemdiensten angewendeten ersetzen oder ersetzen. Durch die geschichtete Struktur von Betriebssystemdiensten, die das Text Layout unterstützen, kann eine Anwendung die zu verwendenden Layoutinformationen auswählen und auswählen, wie Sie angewendet werden soll. Weitere Informationen finden Sie in der [Übersicht über die Microsoft-typografiespezifikationen](https://www.microsoft.com/typography/SpecificationsOverview.mspx) oder die [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu uniscri](about-uniscribe.md)
</dt> </dl>

 

 




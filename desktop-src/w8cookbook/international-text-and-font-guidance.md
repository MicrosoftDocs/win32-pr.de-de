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
# <a name="international-text-and-font-guidance"></a>Leitfaden für internationale Text-und Schriftarten

## <a name="affected-platforms"></a>Betroffene Plattformen

<dl> Clients-Windows 8 \| Windows 8.1  
Server-Windows Server 2012 \| Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Seit Windows 2000 wurde in jeder Hauptversion von Windows eine Textanzeige Unterstützung für neue Skripts hinzugefügt. Sie finden Beschreibungen der Änderungen, die in den einzelnen Hauptversionen des Artikels [Skript-und Schriftart Unterstützung für Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) im Artikel zum [globalen Entwicklungs Center von Go](https://msdn.microsoft.com/goglobal/default)vorgenommen wurden.

Beachten Sie, dass die Unterstützung für ein Skript bestimmte Änderungen an Text Stapel Komponenten und Änderungen an Schriftarten erfordern kann. Das Windows-Betriebssystem verfügt über viele Text Stapel Komponenten: DirectWrite, GDI, uniscri, GDI+, WPF, RichEdit, ComCtl32 und andere. Die bereitgestellten Informationen betreffen hauptsächlich GDI und DirectWrite. Dies gilt auch für Benutzeroberflächen-Frameworks wie RichEdit oder den MSHTML-renderingagent, der für Windows 8 Store-Apps und für das Rendern von Webinhalt verwendet wird, obwohl diese Komponenten möglicherweise bestimmte Unterschiede aufweisen.

## <a name="best-practices"></a>Bewährte Methoden

**Typografieanleitung für Entwickler**

Typografie ist der Kern der Microsoft-Entwurfs Sprache. Jedes der Microsoft-Entwurfs Prinzipien stärkt die Wichtigkeit der Typografie. Zum ersten Mal verfügen App-Entwickler über eine Reihe von Frameworks, die erweiterte typografische Features unterstützen. Informationen zur Verwendung von JavaScript und HTML zum Anzeigen und Bearbeiten von Text in Windows Store-Apps finden Sie unter [anzeigen und](/previous-versions/windows/apps/hh465442(v=win.10)) Bearbeiten von Text.

**Schriftmetriken**

Die Schriftart Metrik ist ein Bereich, der für Anwendungsentwickler besonders wichtig ist. Schriftart Dateien enthalten verschiedene Werte im Zusammenhang mit vertikalen und horizontalen Metriken. Diese Werte sind in der [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/) dokumentiert und sind über eine Vielzahl von APIs verfügbar, die in der [Struktur der dwrite- \_ Schriftart \_ Metriken](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) und in der [TextMetric-Struktur](/windows/win32/api/wingdi/ns-wingdi-textmetrica)gefunden werden.

## <a name="resources"></a>Ressourcen

-   [Skript-und Schriftart Unterstützung für Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Go Global Development Center](https://msdn.microsoft.com/goglobal/default)
-   [Anzeigen und Bearbeiten von Text](/previous-versions/windows/apps/hh465442(v=win.10))
-   [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/)
-   [Dwrite- \_ Schriftart \_ metrikstruktur](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [TextMetric-Struktur](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 
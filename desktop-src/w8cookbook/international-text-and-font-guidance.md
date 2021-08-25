---
title: Internationale Text- und Schriftführung
description: Internationale Text- und Schriftführung
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eeeeaf59f777610603787c3b8e6ed248f36810d34fc2026466b72ca57a1883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935400"
---
# <a name="international-text-and-font-guidance"></a>Internationale Text- und Schriftführung

## <a name="affected-platforms"></a>Betroffene Plattformen

<dl> Clients – Windows 8 \| Windows 8.1  
Server – Windows Server 2012 \| Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Seit Windows 2000 wurde in jeder Hauptversion von Windows Textanzeigeunterstützung für neue Skripts hinzugefügt. Beschreibungen der Änderungen, die in den einzelnen Hauptversionen vorgenommen wurden, finden Sie im Artikel [Skript- und Schriftartunterstützung für Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) im [Go Global Development Center.](https://msdn.microsoft.com/goglobal/default)

Beachten Sie, dass die Unterstützung eines Skripts bestimmte Änderungen an Textstapelkomponenten sowie Änderungen an Schriftarten erfordern kann. Das Windows Betriebssystem verfügt über viele Textstapelkomponenten: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 und andere. Die bereitgestellten Informationen beziehen sich hauptsächlich auf GDI und DirectWrite. Sie gilt auch allgemein für Benutzeroberflächenframeworks wie RichEdit oder den MSHTML-Rendering-Agent, der für Windows 8 Store-Apps und für das Rendern von Webinhalten verwendet wird, obwohl diese Komponenten bestimmte Unterschiede aufweisen können.

## <a name="best-practices"></a>Empfehlungen

**Leitfaden zur Typografie für Entwickler**

Typografie ist das Kernstück der Microsoft-Entwurfssprache. Jedes der Microsoft-Entwurfsprinzipien bestätigt die Bedeutung der Typografie. App-Entwickler verfügen zum ersten Mal über eine Reihe von Frameworks, die erweiterte typografische Features unterstützen. Informationen zur Verwendung von JavaScript und HTML zum [Anzeigen und](/previous-versions/windows/apps/hh465442(v=win.10)) Bearbeiten von Text in Windows Store Apps, erfahren Sie unter Anzeigen und Bearbeiten von Text.

**Schriftartmetriken**

Schriftartmetriken sind ein Bereich, der für Anwendungsentwickler von besonderer Bedeutung ist. Schriftartdateien enthalten verschiedene Werte im Zusammenhang mit vertikalen und horizontalen Metriken. Diese Werte sind in der [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/) dokumentiert und werden über eine Vielzahl von APIs verfügbar gemacht, die unter [DWRITE FONT METRICS structure (DWRITE \_ FONT \_ METRICS-Struktur)](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) und [TEXTMETRIC Structure (TEXTMETRIC-Struktur)](/windows/win32/api/wingdi/ns-wingdi-textmetrica)verfügbar gemacht werden.

## <a name="resources"></a>Ressourcen

-   [Skript- und Schriftartunterstützung für Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Go Global Development Center](https://msdn.microsoft.com/goglobal/default)
-   [Anzeigen und Bearbeiten von Text](/previous-versions/windows/apps/hh465442(v=win.10))
-   [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/)
-   [DWRITE \_ FONT \_ METRICS-Struktur](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [TEXTMETRIC-Struktur](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 
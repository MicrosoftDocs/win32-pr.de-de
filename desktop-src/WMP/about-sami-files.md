---
title: Informationen zu Sami-Dateien
description: Informationen zu Sami-Dateien
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Dateien
- Samisch (synchronisierter, zugänglicher Medienaustausch), Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856267"
---
# <a name="about-sami-files"></a>Informationen zu Sami-Dateien

Sami-Dateien sind Textdateien, die eine SMI-oder Sami-Dateinamenerweiterung haben. Sie enthalten die Text Zeichenfolgen, die für synchronisierte Untertitel, Untertitel und Audiobeschreibungen verwendet werden. Außerdem geben Sie die Zeit Steuerungsparameter an, die vom Windows Media Player-Steuerelement verwendet werden, um den Text der geschlossenen Überschrift mit Audioinhalten oder Videoinhalten Wenn eine digitale Mediendatei eine in der Sami-Datei festgelegte Zeit erreicht, ändert sich der Text entsprechend im Anzeigebereich der geschlossenen Beschriftung der Webseite.

Anders als bei einem einfachen Text-Editor (z. b. Microsoft Notepad) ist keine spezielle Software erforderlich, um eine Sami-Datei zu erstellen. In Sami und HTML sind gemeinsame Elemente wie die <HEAD> Tags und gemeinsam <BODY> . Wie in HTML müssen in Sami-Dateien verwendete Tags immer paarweise verwendet werden. Ein Body-Element beginnt z. b. mit einem <BODY> -Tag und muss immer mit einem-Tag enden </BODY> .

Eine grundlegende Sami-Datei erfordert drei grundlegende Tags: <SAMI> , <HEAD> und <BODY> .

Das- <SAMI> Tag identifiziert das Dokument als Sami-Dokument, sodass andere Anwendungen sein Dateiformat erkennen können.

Zwischen den Tags <HEAD> und </HEAD> definieren Sie grundlegende Richtlinien und andere Formatinformationen für das Sami-Dokument, z. b. den Dokumenttitel, allgemeine Informationen und Stileigenschaften für Untertitel. Wie bei HTML wird der innerhalb des Head-Elements deklarierte Inhalt nicht als Ausgabe angezeigt.

Elemente und Attribute, die zwischen den Tags <BODY> und </BODY> definiert sind, zeigen Inhalt an, der vom Benutzer angezeigt wird. In Sami enthält das Body-Element die Parameter für die Synchronisierung und die Text Zeichenfolgen, die für Untertitel verwendet werden.

Das Style-Element, das im Head-Element definiert ist, bietet zusätzliche Funktionen in Sami. Zwischen den Tags und können Sie mehrere Cascading Stylesheet (CSS) <STYLE> - </STYLE> Selektoren für Stil und Layout definieren. Stileigenschaften wie Schriftarten, Größen und Ausrichtungen können angepasst werden, um eine umfangreiche Benutzerfreundlichkeit bereitzustellen und gleichzeitig Barrierefreiheit zu fördern. Wenn Sie z. b. eine große Textschrift Klasse definieren, kann die Lesbarkeit für Benutzer verbessert werden, die Probleme beim Lesen von geringem Text haben. Darüber hinaus können Sie durch die Definition verschiedener Sprachklassen den digitalen Medieninhalt besser verstehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 





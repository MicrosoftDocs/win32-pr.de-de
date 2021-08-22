---
title: Informationen zu SAMI-Dateien
description: Informationen zu SAMI-Dateien
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Objektmodell, Synchronized Accessible Media Interchange (SAMI)
- Objektmodell,Synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player Mobiler, synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Mobile ActiveX,Synchronized Accessible Media Interchange (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronisierter austauschbarer Medienaustausch (SAMI), Dateien
- SAMI (Synchronized Accessible Media Interchange), Files
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcb4823ee02a501254218a9b7c4d9aaf347894d895bc193c8ce763658db174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470460"
---
# <a name="about-sami-files"></a>Informationen zu SAMI-Dateien

SAMI-Dateien sind Textdateien mit der Dateierweiterung SMI oder SAMI. Sie enthalten die Textzeichenfolgen, die für synchronisierte Untertitel, Untertitel und Audiobeschreibungen verwendet werden. Sie geben auch die Zeitsteuerungsparameter an, die vom Windows Media Player verwendet werden, um Untertiteltext mit Audio- oder Videoinhalten zu synchronisieren. Wenn eine digitale Mediendatei einen in der SAMI-Datei festgelegten Zeitpunkt erreicht, ändert sich der Text entsprechend im Anzeigebereich der Untertitel der Webseite.

Neben einem einfachen Text-Editor (z. B. Microsoft Editor) ist keine spezielle Software erforderlich, um eine SAMI-Datei zu erstellen. SAMI und HTML verwenden gemeinsame Elemente, z. B. <HEAD> und <BODY> Schilder. Wie in HTML müssen tags, die in SAMI-Dateien verwendet werden, immer paarweise verwendet werden. Ein BODY-Element beginnt z. B. mit einem <BODY> -Tag und müssen immer mit einem -Tag enden. </BODY> ein.

Eine einfache SAMI-Datei erfordert drei grundlegende Tags: <SAMI> , <HEAD>, und <BODY>.

Das <SAMI> Tag identifiziert das Dokument als SAMI-Dokument, damit andere Anwendungen sein Dateiformat erkennen können.

Zwischen den <HEAD> und </HEAD> -Tags definieren Sie grundlegende Richtlinien und andere Formatinformationen für das SAMI-Dokument, z. B. den Dokumenttitel, allgemeine Informationen und Stileigenschaften für Untertitel. Wie HTML wird der im HEAD-Element deklarierte Inhalt nicht als Ausgabe angezeigt.

Zwischen den definierten Elementen und Attributen <BODY> und </BODY> -Tags zeigen inhalte an, die vom Benutzer angezeigt werden. In SAMI enthält das BODY-Element die Parameter für die Synchronisierung und die Für Untertitel verwendeten Textzeichenfolgen.

Das STYLE-Element, das innerhalb des HEAD-Elements definiert ist, bietet zusätzliche Funktionen in SAMI. Zwischen den <STYLE> Tags und </STYLE> können Sie mehrere CSS-Selektoren (Cascading StyleSheet) für Stil und Layout definieren. Stileigenschaften wie Schriftarten, Größen und Ausrichtungen können angepasst werden, um eine umfassende Benutzererfahrung zu bieten und gleichzeitig die Barrierefreiheit zu fördern. Beispielsweise kann das Definieren einer Großen Textschriftartklasse die Lesbarkeit für Benutzer verbessern, die Schwierigkeiten beim Lesen von kleinem Text haben. Darüber hinaus können Sie durch die Definition verschiedener Sprachklassen internationalen Benutzern helfen, die digitalen Medieninhalte besser zu verstehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 





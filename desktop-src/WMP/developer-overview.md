---
title: Entwicklerübersicht
description: Entwicklerübersicht
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player-Plug-Ins, Visualisierungen
- Plug-Ins, Visualisierungen
- Visualisierungen, Entwicklerübersicht
- Benutzerdefinierte Visualisierungen, Entwicklerübersicht
- Visualisierungen, COM-Steuerelemente
- Benutzerdefinierte Visualisierungen, COM-Steuerelemente
- Visualisierungen, Audioeingabe
- Benutzerdefinierte Visualisierungen, Audioeingabe
- Visualisierungen, grafische Ausgabe
- Benutzerdefinierte Visualisierungen, grafische Ausgabe
- Visualisierungen, Zeichnungstools
- Benutzerdefinierte Visualisierungen, Zeichnungstools
- Visualisierungen, Programmiersprache
- Benutzerdefinierte Visualisierungen, Programmiersprache
- Visualisierungen,Visual C++
- benutzerdefinierte Visualisierungen,Visual C++
- Visualisierungen, Plug-In-Assistent
- Benutzerdefinierte Visualisierungen, Plug-In-Assistent
- Plug-In-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20988a8cf1b7923699ec9cee7990b99840b8acdf9371e74da5940ddb8fc8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579412"
---
# <a name="developer-overview"></a>Entwicklerübersicht

Aus Sicht des Entwicklers sind Visualisierungen Softwareprogramme, die von Windows Media Player bereitgestellte Audiodaten aufnehmen und in Grafiken konvertieren, die dem Benutzer gefallen. Die wichtigsten Themen, die ein Entwickler verstehen muss, um eine neue Visualisierung zu erstellen, sind die folgenden:

## <a name="visualization-packaging"></a>Visualisierungspaketierung

Visualisierungen sind COM-Steuerelemente, die Windows Media Player verwendet, um Audio waveforms in animierte Grafiken in Microsoft Windows umzuwandeln. Die COM-Steuerelemente werden als Microsoft Windows DLLs (Dynamic Link Libraries) gepackt und müssen in der Windows-Registrierung registriert werden. Wenn Windows Media Player ausgeführt wird, werden registrierte benutzerdefinierte Visualisierungen gemäß den Anweisungen der Skin geladen und angezeigt, die Windows Media Player verwendet.

## <a name="audio-input"></a>Audioeingabe

Windows Media Player stellt Ihrem Code Momentaufnahmen der Audiofrequenz und Wellenformdaten in zeitaufwendigen Intervallen in Sekundenbruchteilen zur Verfügung. Das Momentaufnahmeintervall wird intern durch die Windows Media Player bestimmt.

## <a name="graphical-output"></a>Grafische Ausgabe

Die grafische Ausgabe Ihrer Visualisierung ist ein Microsoft Windows Gerätekontext. Dies ist eine Standard-Windows Zeichnungsoberfläche, auf die Sie bei jeder Bereitstellung einer Audiomomentaufnahme zurückgreifen können. Der gesamte Hintergrund Windows Technologie wird für Sie erledigt. Sie müssen lediglich den Gerätekontext mit den bereitgestellten Audiodaten zeichnen.

## <a name="drawing-tools"></a>Zeichentools

Sie können den Gerätekontext mit Standardfunktionen von Microsoft Windows Graphics Device Interface (GDI) zeichnen, indem Sie Stifte und Pinsel verwenden, um Entwürfe zu erstellen, die von den Audiodaten geändert werden, die Ihnen von Windows Media Player bereitgestellt werden. GDI bietet einen umfangreichen Satz von Zeichentools, die viele Arten visueller Effekte erzeugen können.

## <a name="programming-language"></a>Programmiersprache

Microsoft Visual C++ 6.0 und höher ist die einzige unterstützte Sprache zum Erstellen benutzerdefinierter Visualisierungen.

## <a name="plug-in-wizard"></a>Plug-In-Assistent

Windows Media Player stellt einen COM-Assistenten bereit, den Sie Visual C++ hinzufügen können, der den zugrunde liegenden Code generiert, der für Die Visualisierung benötigt wird. Es werden nicht nur alle Quelldateien bereitgestellt, sondern es wird auch eine Beispielskin generiert, um das Testen Ihrer Visualisierung zu vereinfachen. Der generierte Code erstellt eine Visualisierung ähnlich wie Balken mit zwei Voreinstellungen. Anschließend können Sie den Code ändern, um Ihre eigene Visualisierung zu erstellen. Außerdem wird eine Registrierungsdatei generiert, um Ihre Visualisierung zu registrieren, damit Windows Media Player sie laden können.

Im folgenden Thema wird beschrieben, wie Der Visualisierungscode Audiodaten verarbeitet:

-   [Flow des Steuerelements](flow-of-control.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu benutzerdefinierten Visualisierungen**](about-custom-visualizations.md)
</dt> </dl>

 

 





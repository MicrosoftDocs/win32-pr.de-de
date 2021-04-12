---
title: Entwickler Übersicht
description: Entwickler Übersicht
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player-Plug-ins, Visualisierungen
- Plug-ins, Visualisierungen
- Visualisierungen, Übersicht über Entwickler
- benutzerdefinierte Visualisierungen, Übersicht über Entwickler
- Visualisierungen, com-Steuerelemente
- benutzerdefinierte Visualisierungen, com-Steuerelemente
- Visualisierungen, Audioeingabe
- benutzerdefinierte Visualisierungen, Audioeingabe
- Visualisierungen, grafische Ausgabe
- benutzerdefinierte Visualisierungen, grafische Ausgabe
- Visualisierungen, Zeichnungs Tools
- benutzerdefinierte Visualisierungen, Zeichnungs Tools
- Visualisierungen, Programmiersprache
- benutzerdefinierte Visualisierungen, Programmiersprache
- Visualisierungen, Visual C++
- benutzerdefinierte Visualisierungen, Visual C++
- Visualisierungen, Plug-in-Assistent
- benutzerdefinierte Visualisierungen, Plug-in-Assistent
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310599"
---
# <a name="developer-overview"></a>Entwickler Übersicht

Aus Sicht des Entwicklers sind Visualisierungen Softwareprogramme, die von Windows bereitgestellte Audiodaten akzeptieren Media Player und diese Daten in Grafiken konvertieren, um den Benutzer zu überwachen. Die wichtigsten Aspekte, die ein Entwickler kennen muss, um eine neue Visualisierung zu erstellen, sind die folgenden:

## <a name="visualization-packaging"></a>Visualisierungs Verpackung

Visualisierungen sind com-Steuerelemente, die von Windows Media Player verwendet werden, um Audiowellen Formen in animierte Grafiken in Microsoft Windows umzuwandeln. Die com-Steuerelemente werden als Microsoft Windows Dynamic-Link Libraries (DLLs) verpackt und müssen in der Windows-Registrierung registriert werden. Beim Ausführen von Windows Media Player werden registrierte benutzerdefinierte Visualisierungen geladen und entsprechend den Anweisungen der von Windows Media Player verwendeten Skin angezeigt.

## <a name="audio-input"></a>Audioeingabe

Windows Media Player bietet Ihren Code Momentaufnahmen von audiohäufigkeit und Wellenform Daten in zeitlich begrenzten Intervallen, gemessen in Sekundenbruchteilen. Das Momentaufnahme Intervall wird intern vom Windows-Media Player festgelegt.

## <a name="graphical-output"></a>Grafische Ausgabe

Die grafische Ausgabe der Visualisierung ist ein Microsoft Windows-Gerätekontext. Dies ist eine standardmäßige Windows-Zeichen Oberfläche, die Sie bei jeder Bereitstellung einer audiomomentaufnahme zeichnen können. Alle Hintergrund-Windows-Technologien werden für Sie erledigt. Sie müssen lediglich den Gerätekontext mit den bereitgestellten Audiodaten zeichnen.

## <a name="drawing-tools"></a>Zeichnungs Tools

Sie können den Gerätekontext mit standardmäßigen Microsoft Windows Graphics Device Interface (GDI)-Funktionen zeichnen, indem Sie Stifte und Pinsel verwenden, um Entwürfe zu erstellen, die von den Audiodaten geändert werden, die Ihnen von Windows Media Player bereitgestellt werden. GDI stellt einen umfangreichen Satz von Zeichnungs Tools bereit, die viele Arten von visuellen Effekten erzeugen können.

## <a name="programming-language"></a>Programmiersprache

Microsoft Visual C++ 6,0 und höher ist die einzige unterstützte Sprache zum Erstellen von benutzerdefinierten Visualisierungen.

## <a name="plug-in-wizard"></a>Plug-in-Assistent

Windows Media Player stellt einen com-Assistenten bereit, den Sie Visual C++ hinzufügen können, der den zugrunde liegenden Code generiert, der für ihre Visualisierung benötigt wird. Es werden nicht nur alle Quelldateien bereitgestellt, sondern es wird eine Beispiel Skin generiert, um das Testen der Visualisierung zu erleichtern. Der generierte Code erstellt eine Visualisierung ähnlich wie Balken mit zwei Voreinstellungen. Anschließend können Sie den Code ändern, um eine eigene Visualisierung zu erstellen. Außerdem wird eine Registrierungsdatei generiert, um die Visualisierung zu registrieren, sodass Sie von Windows Media Player geladen werden kann.

Im folgenden Thema wird beschrieben, wie Visualisierungs Code Audiodaten verarbeitet:

-   [Ablauf Steuerung](flow-of-control.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu benutzerdefinierten Visualisierungen**](about-custom-visualizations.md)
</dt> </dl>

 

 





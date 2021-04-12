---
title: VML-Einführung
description: VML-Einführung
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Vector Markup Language (VML), Referenz
- VML (Vector Markup Language), Referenz
- Vektorgrafiken, VML-Referenz
- Vektorgrafiken, Vector Markup Language (VML)
- Referenz für Vector Markup Language (VML)
- VML-Referenz
- Vector Markup Language (VML), Shape-Element
- VML (Vector Markup Language), Shape-Element
- Vektorgrafiken, Shape-Element
- Shape-Element
- VML-Elemente, Form
- Vector Markup Language (VML), VBScript
- VML (Vector Markup Language), VBScript
- Vector Markup Language (VML), JavaScript
- VML (Vector Markup Language), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390474"
---
# <a name="vml-introduction"></a>VML-Einführung

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Dieses Dokument enthält einen umfassenden detaillierten Verweis auf die Implementierung der Vector Markup Language (VML), die mit Microsoft Office 2000 ausgeliefert wird. Andere Implementierungen können variieren. Weitere Informationen zu VML als Standard finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-datetime.html) .

VML ist als Satz von XML-Elementen und den entsprechenden Attributen für jedes Element definiert. Da das **Shape** -Element der grundlegende Baustein von VML ist, klicken Sie [hier](shape-element--vml.md) , um den Verweis zu beginnen.

Beachten Sie, dass dieser Verweis mehrere Beispiele und Demos enthält. Sie müssen Microsoft Internet Explorer 5,0 oder höher installiert haben, um die Live-VML anzuzeigen.

Zusätzlich zu den Informationen zur Verwendung von Elementen und Attributen als XML-Tags, die HTML erweitern, enthält diese Referenz Syntax und Beispiele, die zeigen, wie die Skripterstellung und die Dokumentobjektmodell Features von Internet Explorer 5 oder höher verwendet werden. Die Verwendung von Skripts mit VML ermöglicht das dynamische Erstellen von Elementen und das Bearbeiten von Attributen in Echtzeit.

In diesen Beispielen in dieser Referenz werden VBScript und JavaScript verwendet. Wenn Sie eine andere Skriptsprache verwenden, als in einem Beispiel gezeigt, müssen Sie die Groß-/Kleinschreibung aller Element-und Attributnamen vergleichen. Der Verweis gibt Skript Syntax, die für Sprachen mit Unterscheidung nach Groß-/Kleinschreibung wie JavaScript korrekt ist. Wenn Sie sich im Zweifelsfall bezüglich des richtigen Zeichen Falls befinden, verwenden Sie einen Objektkatalog (z. b. OLEVIEW), um die VGX.DLL zu untersuchen, um die genaue Groß-/Kleinschreibung eines Elements oder Beachten Sie, dass bei Verwendung von VML als XML-Tags die Groß-/Kleinschreibung abhängig vom Dokumenttyp des zugrunde liegenden Dokuments ist. Wenn Sie einen Strict-Modus verwenden! Bei DOCTYPE, Elementen und Attributen wird die Groß-/Kleinschreibung beachtet.

[VML-Referenz](shape-element--vml.md)

 

 
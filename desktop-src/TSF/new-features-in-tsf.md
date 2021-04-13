---
title: Neue Features in TSF
description: Mit der Veröffentlichung von Microsoft WindowsXP Service Pack 1 bietet das Text Services-Framework (TSF) mehrere neue Features.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Text Services Framework (TSF), neue Features
- TSF (Text Dienst Framework), neue Features
- Text Dienste, neue Features
- TSF-aktivierte Anwendungen, neue Features
- Text Services Framework (TSF), erweiterter Support
- TSF (Text Dienst Framework), erweiterter Support
- Text Dienste, erweiterter Support
- TSF-fähige Anwendungen, erweiterter Support
- Text Services-Framework (TSF), umfangreiche Bearbeitung
- TSF (Text Dienst Framework), umfangreiche Bearbeitung
- Text Dienste, umfangreiche Bearbeitung
- TSF-fähige Anwendungen, umfangreiche Bearbeitung
- Umfassende Bearbeitung
- Text Dienst Framework (TSF), Sicherheit
- TSF (Text Dienst Framework), Sicherheit
- Text Dienste, Sicherheit
- TSF-aktivierte Anwendungen, Sicherheit
- Sicherheit für TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390409"
---
# <a name="new-features-in-tsf"></a>Neue Features in TSF

Mit der Veröffentlichung von Microsoft WindowsXP Service Pack 1 bietet das Text Services-Framework (TSF) mehrere neue Features.

## <a name="extended-support-of-advanced-text-services"></a>Erweiterter Support für erweiterte Text Dienste

Es wurde Unterstützung für TSF und Windows hinzugefügt, um eine konsistente Benutzeroberfläche für alle Anwendungen auf dem Desktop bereitzustellen. Mit dieser neuen Unterstützung können ältere Anwendungen oder Steuerelemente, die TSF nicht kennen, einige erweiterte Text Dienste kostenlos nutzen. Beispielsweise können die sprach Diktat-und Handschrift nun verwendet werden, um Text in ein Dokument in einer beliebigen Anwendung einzugeben.

Dieses neue Feature ist nur für den Windows XP-Dienst Pack 1 oder höher verfügbar. Sie ist standardmäßig deaktiviert. Um es zu aktivieren, aktivieren Sie das Kontrollkästchen auf der neuen Registerkarte " **erweitert** " im Bereich **Text Dienste und Eingabe Sprachen** der Systemsteuerung Regions **-und Sprachoptionen** .

![nicht unterstützte Anwendungsunterstützung in der TSF-Systemsteuerung](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Umfangreiche Bearbeitungs Unterstützung

[Microsoft® reichhaltige Bearbeitung](../controls/rich-edit-controls.md) Version 4,1, die von Anwendungen verwendet wird, um Text mit Sonderzeichen-und Absatz Formatierung anzuzeigen und zu bearbeiten, stellt nun die TSF-Funktionalität zur Verfügung. Diese Unterstützung ist standardmäßig deaktiviert. Zum Aktivieren von TSF in Rich Edit sendet eine Hostinganwendung eine spezielle Fenster Meldung an das Rich Edit-Steuerelement.

## <a name="security-improvements"></a>Sicherheitsverbesserungen

Die Sicherheit und Stabilität von TSF wurden erheblich verbessert, um die Wahrscheinlichkeit zu verringern, dass ein schädliches Programm auf den Stapel, Heap oder andere sichere Speicherorte zugreifen kann. Die Security of Software Development Kit (SDK)-Beispielanwendungen und Text Dienste wurden ebenfalls verbessert.

 

 
---
title: Neue Features in TSF
description: Mit der Veröffentlichung von Microsoft WindowsXP Service Pack1 verfügt Textdienstframework (TSF) über mehrere neue Features.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Textdienstframework (TSF), neue Features
- TSF (Textdienstframework),neue Features
- Textdienste, neue Features
- TSF-fähige Anwendungen, neue Features
- Textdienstframework (TSF), erweiterte Unterstützung
- TSF (Textdienstframework),erweiterte Unterstützung
- Textdienste, erweiterte Unterstützung
- TSF-fähige Anwendungen, erweiterte Unterstützung
- Textdienstframework (TSF), Rich Edit
- TSF (Textdienstframework),Rich Edit
- Textdienste,Rich Edit
- TSF-fähige Anwendungen, Rich Edit
- Rich Edit
- Textdienstframework (TSF),Sicherheit
- TSF (Textdienstframework),Sicherheit
- Textdienste,Sicherheit
- TSF-fähige Anwendungen, Sicherheit
- Sicherheit für TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73494d4538b25dfa0b004c8691391fb1c572c7ce6d82247cacae4fb9e0a838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952021"
---
# <a name="new-features-in-tsf"></a>Neue Features in TSF

Mit der Veröffentlichung von Microsoft WindowsXP Service Pack1 verfügt Textdienstframework (TSF) über mehrere neue Features.

## <a name="extended-support-of-advanced-text-services"></a>Erweiterte Unterstützung erweiterter Textdienste

Die Unterstützung für TSF und Windows wurde hinzugefügt, um eine konsistente Benutzeroberfläche für alle Anwendungen auf dem Desktop bereitzustellen. Diese neue Unterstützung ermöglicht es Legacyanwendungen oder Steuerelementen, die tsf nicht kennen, einige erweiterte Textdienste kostenlos zu nutzen. Beispielsweise können Sprachdiktat und Handschrift jetzt verwendet werden, um Text in ein Dokument in einer beliebigen Anwendung einzugeben.

Dieses neue Feature ist nur für WindowsXP Service Pack1 oder höher verfügbar. Sie ist standardmäßig deaktiviert. Um dies zu aktivieren, aktivieren Sie das Kontrollkästchen auf der neuen Registerkarte **Erweitert** im Bereich **Textdienste und Eingabesprachen** der Systemsteuerung **Regionale optionen und Sprachoptionen.**

![Unterstützung nicht bekannter Anwendungen in der TSF-Systemsteuerung](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Rich Edit-Unterstützung

[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, die von Anwendungen zum Anzeigen und Bearbeiten von Text mit Sonderzeichen- und Absatzformatierung verwendet wird, macht jetzt TSF-Funktionen verfügbar. Standardmäßig ist diese Unterstützung deaktiviert. Um TSF in Rich Edit zu aktivieren, sendet eine Hostinganwendung eine spezielle Fenstermeldung an das Rich Edit-Steuerelement.

## <a name="security-improvements"></a>Sicherheitsverbesserungen

Die Sicherheit und Stabilität von TSF wurde erheblich verbessert, um die Wahrscheinlichkeit zu verringern, dass ein schädliches Programm auf den Stapel, Heap oder andere sichere Speicherorte zugreifen kann. Die Sicherheit von Sdk-Beispielanwendungen und Textdiensten (Software Development Kit) wurde ebenfalls verbessert.

 

 
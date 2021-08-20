---
title: Zuordnen Waveform-Audio Geräten
description: Zuordnen Waveform-Audio Geräten
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- Multimediaaudio, Zuordnen von Waveform-Audiogeräten
- Audio, Zuordnen von Waveform-Audio-Geräten
- Audiokomprimierungs-Manager (ACM), Zuordnen von Waveform-Audiogeräten
- ACM (Audiokomprimierungs-Manager),Zuordnen von Waveform-Audiogeräten
- Zuordnen von Waveform-Audiogeräten
- Multimediaaudio, Mapper
- Audio, Mapper
- Audiokomprimierungs-Manager (ACM), Mapper
- ACM (Audiokomprimierungs-Manager),Mapper
- mapper
- Waveformaudio, Geräte zuordnen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4204a79eebd5fed3c8f96712aa3cd83c50056b1c194bafe2ce485a5b4b68f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138771"
---
# <a name="mapping-waveform-audio-devices"></a>Zuordnen Waveform-Audio Geräten

Windows bietet eine Reihe von Standardfunktionen für Audiogeräte. Diese Funktionen führen Aufrufe an Gerätetreiber aus, die Hardwaregeräte verwalten. Das System verwendet ein Modul namens "Mapper", um installierte Geräte zu verwalten. Der Mapper verwendet spezielle Hooks in der Treiberschnittstelle, um Aufrufe abzufangen und als Vermittler zwischen dem System und den im System installierten Treibern zu fungieren. Der Mapper ist dafür verantwortlich, die Anforderungen einer Anwendung für den Zugriff auf ein Gerät mit den verfügbaren Geräten abzugleichen und ein Gerät zu finden, das die Audioanforderungen der aktuellen Anwendung erfüllt. Das System stellt Mapper für Standardtreibertypen bereit: Waveform-Audio, DISCOUNT (Instruments Instrument Digital Interface) und Hilfsgeräte.

Der ACM ist eine Erweiterung des grundlegenden Multimediasystems und wird als Mapper installiert. Dies bedeutet, dass der ACM die Hooks der Treiberschnittstellenzuordnung für Waveform-Audio-Geräte verwendet. Die Verwendung dieser Hooks ermöglicht dem ACM das Decodieren oder Codieren von Waveform-Audio-Daten, bevor diese an einen oder von einem Waveform-Audio-Gerätetreiber übergeben werden. Der Unterschied zwischen dem ACM und der Standardsystemzuordnung besteht darin, dass der ACM nach einem Waveform-Audiogerät suchen kann, das ein angegebenes Format unterstützt, oder eine Kombination aus einem Waveform-Audio-Gerät und einem ACM-Audiogerät oder -Dekomprimierer finden kann, der ein angegebenes Format unterstützt.

Wenn eine Anwendung anfordert, dass das System ein Waveform-Audiogerät für die Eingabe oder Ausgabe öffnet, gibt die Anforderung das Format und das Gerät an. Wenn das angegebene Gerät der Mapper ist, muss der Mapper ein Gerät finden, das das angegebene Format unterstützt. Der im ACM implementierte Mapper sucht nach einem installierten Waveform-Audio-Gerät, das das angegebene Format unterstützt. Wenn der ACM ein solches Gerät nicht finden kann, sucht er nach einem Waveform-Audio-Gerät und einer Sprech- oder Dekomprimierung, die zusammen das Format unterstützen. Insbesondere sucht der ACM nach einem Zieh- oder Dekomprimierer, der das angegebene Format in ein Format konvertiert, das von einem installierten Waveform-Audiogerät unterstützt wird. Nachdem der ACM ein Gerät gefunden hat, das das konvertierte Format unterstützt, kann er Anforderungen zum Wiedergeben oder Aufzeichnen des ursprünglich angeforderten Formats einhalten, obwohl kein installiertes Waveform-Audiogerät dieses Format direkt unterstützt.

Zusätzlich zur Formatkonvertierung bietet der ACM auch Dienste zur Unterstützung von Komprimierung, Dekomprimierung, Filterung, Formatauswahl und Filterauswahl. Sie stellt eine Standard-API bereit, die sie unterstützt, indem sie ihre eigenen Treiber aufruft.

 

 





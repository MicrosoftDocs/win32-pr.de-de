---
description: Auswählen des DVD-Bereichs durch Microsoft DVD Navigator
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Auswählen des DVD-Bereichs durch Microsoft DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343120"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Auswählen des DVD-Bereichs durch Microsoft DVD Navigator

Der Microsoft DVD Navigator verwendet den folgenden Algorithmus, um die Regions Übereinstimmung bei der Wiedergabe von DVD-CDs auf einem PC zu bestimmen

1.  Der DVD-Navigator Ruft den Bereich für die Festplatte, den Laufwerk Bereich und den decoderbereich ab.
2.  Wenn der Festplatten Bereich "alle Regionen" ist, gibt der DVD-Navigator die Festplatte aus.
3.  Wenn die Festplatte nicht für alle Regionen markiert ist, überprüft der DVD-Navigator, ob der Decoder einen voreingestellten Bereich aufweist.
4.  Wenn der Decoder einen voreingestellten Bereich hat, der nicht mit dem Bereich der Festplatte identisch ist, gibt der DVD-Navigator einen Fehler zurück, der anzeigt, dass er die CD nicht in der aktuellen DVD-Konfiguration wiedergeben kann Abstiegs
5.  Wenn der decoderbereich nicht festgelegt ist oder mit dem Bereich der Festplatte identisch ist, überprüft der DVD-Navigator, ob der Laufwerks Bereich mit dem Bereich der Festplatte identisch ist.
6.  Wenn die Laufwerks Region mit dem Bereich der Festplatte übereinstimmt, gibt der DVD-Navigator den Titel wieder.
7.  Andernfalls ruft der DVD-Navigator den Code auf, wenn der Treiber Bereich nicht mit dem Bereich der Festplatte identisch ist, um den Bereich des Laufwerks zu ändern. Wenn die zulässige Anzahl von Regions Änderungen ausgeschöpft ist, tritt beim Änderungs Versuch der Region ein Fehler auf, und der Titel kann auf diesem System nicht wiedergegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung der Änderung von DVD-Regionen in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




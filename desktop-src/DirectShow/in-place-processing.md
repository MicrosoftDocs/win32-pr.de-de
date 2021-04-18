---
description: In-Place Verarbeitung
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340083"
---
# <a name="in-place-processing"></a>In-Place Verarbeitung

Bestimmte Daten Transformationen können durch direktes Ändern der Daten erreicht werden. Dies *wird als direkte Verarbeitung bezeichnet* . Viele Audio-und Video Effekte können auf diese Weise ausgeführt werden. Wenn ein DMO die direkte Verarbeitung unterstützt, wird die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle verfügbar gemacht. Die direkte Verarbeitung ist im Allgemeinen effizienter als die Verwendung separater Puffer für die Ausgabe. (Eine wichtige Ausnahme ist, wenn sich der Puffer im Videospeicher befindet. In dieser Situation sind Lesevorgänge viel langsamer als Schreibvorgänge, sodass die direkte Verarbeitung nicht empfohlen wird.

Zum Verarbeiten von Daten führt der Client einen einzigen Aufruf an die [**imediaobjectinplace::P rocess**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) -Methode anstelle von separaten Aufrufen von **ProcessInput** und **ProcessOutput** aus. Die **Prozess** Methode ist synchron. die gesamte Verarbeitung erfolgt innerhalb des Aufrufes. Außerdem werden bei der direkten Verarbeitung keine **imediabuffer** -Objekte verwendet. Die **Process** -Methode nimmt einen Zeiger direkt auf den Speicherpuffer an.

Ein DMO, der die direkte Verarbeitung unterstützt, muss immer noch die **imediaobject** -Schnittstelle implementieren, einschließlich der Methoden **ProcessInput** und **ProcessOutput** . Der Client kann auswählen, ob die direkte Verarbeitung verwendet oder separate Puffer verwendet werden sollen. Kombinieren Sie die beiden Verarbeitungs Typen jedoch nicht. Wenn Sie **Process** aufrufen, dürfen Sie **ProcessInput** oder **ProcessOutput** nicht aufrufen und umgekehrt.

**Effekt-Tails**

Ein direkter DMO erstellt möglicherweise eine zusätzliche Ausgabe, nachdem die Eingabe angehalten wurde. Dies wird als *Effekt* Ende bezeichnet. Beispielsweise wird ein Hall Effekt fortgesetzt, nachdem die Eingabe den Ruhe- Wenn ein Effekt Ende vorliegt, gibt die **Process** -Methode den Wert "false" zurück \_ . Nachdem die Anwendung alle Daten verarbeitet hat, kann Sie das Effekt Ende generieren, indem leere Puffer an die **Prozess** Methode gesendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosting eines DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 




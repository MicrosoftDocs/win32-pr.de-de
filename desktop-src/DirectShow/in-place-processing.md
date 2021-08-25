---
description: In-Place Verarbeitung
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1a72b6bad2311a9c96bdd94e7e63acdc7e4961b51e106324dbe38de9510ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818795"
---
# <a name="in-place-processing"></a>In-Place Verarbeitung

Bestimmte Datentransformationen können durch direktes Ändern der Daten durchgeführt werden. Dies wird als *"In-Place-Verarbeitung"* bezeichnet. Viele Audio- und Videoeffekte können auf diese Weise durchgeführt werden. Wenn ein DMO die verarbeitung direkt unterstützt, macht er die [**IMediaObjectInPlace-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) verfügbar. Die verarbeitung vor Ort ist im Allgemeinen effizienter als die Verwendung separater Puffer für die Ausgabe. (Eine hauptausnahme ist, wenn sich der Puffer im Videospeicher befindet. In diesem Fall sind Lesevorgänge viel langsamer als Schreibvorgänge, daher wird keine verarbeitung vor Ort empfohlen.)

Um Daten direkt zu verarbeiten, ruft der Client die [**IMediaObjectInPlace::P rocess-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) auf, anstatt die Aufrufe von **ProcessInput** und **ProcessOutput voneinander zu trennen.** Die **Process-Methode** ist synchron. die Verarbeitung erfolgt innerhalb des Aufrufs. Außerdem werden bei der direkt verarbeiteten Verarbeitung keine **IMediaBuffer-Objekte** verwendet. Die **Process-Methode** verwendet einen Zeiger direkt auf den Speicherpuffer.

Ein DMO, der die verarbeitung direkt unterstützt, muss weiterhin die **IMediaObject-Schnittstelle** implementieren, einschließlich der **Methoden ProcessInput** und **ProcessOutput.** Der Client kann auswählen, ob die in-place-Verarbeitung oder separate Puffer verwendet werden. Mischen Sie jedoch nicht die beiden Verarbeitungstypen. Wenn Sie **Process aufrufen,** rufen Sie **processInput** oder **ProcessOutput** nicht auf und umgekehrt.

**Effect Tails**

Eine in-place-DMO erstellt möglicherweise eine zusätzliche Ausgabe, nachdem die Eingabe beendet wurde. Dies wird als *Effektende bezeichnet.* Beispielsweise wird ein Halleffekt fortgesetzt, nachdem die Eingabe Stille erreicht hat. Wenn ein Effektende vorkommt, gibt **die Process-Methode** S \_ FALSE zurück. Nachdem die Anwendung alle Daten verarbeitet hat, kann sie das Effektende generieren, indem leere Puffer an die **Process-Methode senden.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosten DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 




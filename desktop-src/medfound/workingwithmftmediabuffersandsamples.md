---
description: Arbeiten mit MFT-Medienpuffern und -Beispielen
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Arbeiten mit MFT-Medienpuffern und -Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964f1c2f2a5fd5f92d5af87213c6977fc51bee76caf3a281861788e2a2fb922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736451"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Arbeiten mit MFT-Medienpuffern und -Beispielen

Codec-MFTs übergeben Mediendaten mithilfe von Medienpuffern und Samplings hin und her.

Ein Medienpuffer ist ein COM-Objekt, das einen Speicherblock verwaltet, in der Regel zum Speichern von Mediendaten. Wenn Daten an oder von einem MFT übergeben werden, werden sie immer in Form eines Medienpuffers übergeben.

Alle Medienpuffer machen die **INTERFACESMediaBuffer-Schnittstelle** verfügbar. Diese Schnittstelle ist für jeden Datentyp konzipiert. Puffer, die Videodaten enthalten, machen häufig auch **DEN 2DBuffer verfügbar.**

Ein Medienpuffer hat eine maximale Größe, d. h. die Menge an Arbeitsspeicher, die dem Puffer zugeordnet ist. Rufen Sie ZUM Ermitteln der maximalen Größe **DEN AUFRUF VONMEDIABUFFER::GetMaxLength** auf. Zu jedem Zeitpunkt verfügt ein Medienpuffer auch über eine aktuelle Länge, d. h. die Menge gültiger Daten im Puffer, die zwischen null Bytes und der maximalen Größe liegen. Rufen Sie ZUM Abrufen der aktuellen Länge **DEN AUFRUF VONMEDIABUFFER::GetCurrentLength** auf. Wenn der Puffer erstellt wird, ist die aktuelle Länge 0 (null). Wenn Sie Daten in den Puffer schreiben, rufen Sie **ÜBERMEDIABUFFER::SetCurrentLength** auf, um die aktuelle Länge zu aktualisieren.

Rufen Sie ZUM Zugreifen auf den Arbeitsspeicher im Puffer **DEN AUFRUF VONMEDIABUFFER::Lock** auf. Diese Methode gibt einen Zeiger auf den Anfang des Speicherblocks zurück. Wenn Sie die Verwendung des Zeigers abgeschlossen haben, rufen Sie **DENMEDIABUFFER::Unlock** auf. Die **Lock-Methode** ist kein Threadsynchronisierungsmechanismus. sie garantiert nicht, dass andere Threads nicht auf den Puffer zugreifen können. Die **Lock-Methode** wird verwendet, um sicherzustellen, dass der Arbeitsspeicher, auf den zugegriffen wird, gültig bleibt, bis Sie die **Unlock-Methode** aufrufen.

Ein Medienbeispielobjekt (im Kontext des Media Foundation SDK) ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält. Medienbeispiele machen die **INTERFACESSample-Schnittstelle** verfügbar.

Um ein neues Beispiel zu erstellen, rufen Sie die **MFCreateSample-Funktion** auf. Anfänglich ist die Pufferliste des Beispiels leer. Rufen Sie ZUM Hinzufügen eines Puffers am Ende der Liste **DEN AUFRUF VONSAMPLE::AddBuffer auf.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 




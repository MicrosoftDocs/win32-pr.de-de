---
description: Arbeiten mit MFT-Medien Puffern und-Beispielen
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Arbeiten mit MFT-Medien Puffern und-Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351338"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Arbeiten mit MFT-Medien Puffern und-Beispielen

Codec-MFTs übergeben Mediendaten mithilfe von Medien Puffern und Beispielen hin und her.

Ein Medien Puffer ist ein COM-Objekt, das einen Speicherblock verwaltet, der normalerweise Mediendaten enthält. Wenn Daten an oder von einem MFT-Wert übermittelt werden, werden Sie immer in Form eines Medien Puffers übermittelt.

Alle Medien Puffer machen die **imfmediabuffer** -Schnittstelle verfügbar. Diese Schnittstelle ist für beliebige Datentypen konzipiert. Puffer mit Videodaten machen häufig auch **IMF2DBuffer** verfügbar.

Ein Medien Puffer hat eine maximale Größe, die der für den Puffer zugeordneten Arbeitsspeicher Menge entspricht. Um die maximale Größe zu ermitteln, nennen Sie **imfmediabuffer:: getmaxlength**. Ein Medien Puffer hat zu einem beliebigen Zeitpunkt auch eine aktuelle Länge, d. h. die Menge gültiger Daten im Puffer, von 0 Bytes bis zur maximalen Größe. Um die aktuelle Länge abzurufen, nennen Sie **imfmediabuffer:: getcurrentlength**. Beim Erstellen des Puffers ist die aktuelle Länge 0 (null). Wenn Sie Daten in den Puffer schreiben, müssen Sie **imfmediabuffer:: setcurrentlength** aufrufen, um die aktuelle Länge zu aktualisieren.

Um auf den Speicher im Puffer zuzugreifen, nennen Sie **imfmediabuffer:: Lock**. Diese Methode gibt einen Zeiger auf den Anfang des Speicherblocks zurück. Wenn Sie die Verwendung des Zeigers abgeschlossen haben, nennen Sie **imfmediabuffer:: Unlock**. Die **Lock** -Methode ist kein Thread Synchronisierungs Mechanismus. Es ist nicht gewährleistet, dass andere Threads nicht auf den Puffer zugreifen können. Mithilfe der **Lock** -Methode wird sichergestellt, dass der Speicher, auf den zugegriffen wird, gültig bleibt, bis Sie die **Unlock** -Methode aufrufen.

Ein Medien Beispiel Objekt (im Kontext des Media Foundation SDK) ist ein Objekt, das eine geordnete Liste von 0 (null) oder mehr Puffern enthält. In Medien Beispielen wird die **IMF Sample** -Schnittstelle verfügbar gemacht.

Um ein neues Beispiel zu erstellen, rufen Sie die **mfkreatesample** -Funktion auf. Anfänglich ist die Puffer Liste des Beispiels leer. Um einen Puffer am Ende der Liste hinzuzufügen, nennen Sie **imfsample:: addbuffer**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 




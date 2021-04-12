---
description: Arbeiten mit MFT-Medientypen
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Arbeiten mit MFT-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218978"
---
# <a name="working-with-mft-media-types"></a>Arbeiten mit MFT-Medientypen

Ein Medientyp ist eine Möglichkeit, das Format eines Mediendaten Stroms zu beschreiben. In Media Foundation werden Medientypen durch die **IMF MediaType** -Schnittstelle dargestellt. Diese Schnittstelle erbt die **imfattributes** -Schnittstelle. Die Details eines Medientyps werden als Attribute angegeben.

Um einen neuen Medientyp zu erstellen, rufen Sie die **mfkreatemediatype** -Funktion auf. Diese Funktion gibt einen Zeiger auf die **imfmediatype** -Schnittstelle zurück. Der Medientyp hat anfänglich keine Attribute.

Das Media Foundation SDK bietet mehrere Hilfsfunktionen zum Initialisieren von Medientypen aus Format Strukturen. Beispielsweise initialisiert die Funktion " **mfinitmediatyetfromvideoinfoheader** " einen Videotyp aus einer **videoinfoheader** -Struktur, und die Funktion " **mfinitmediatypeer fromwaveformatex** " Initialisiert einen Videotyp aus einer **WaveFormatEx** -oder **WAVEFORMATEXTENSIBLE** -Struktur.

Die von den Codecs verwendeten Format Typen sind in der Regel auf die von den **videoinfoheader** -und **WaveFormatEx** -Strukturen beschriebenen Typen beschränkt.

Weitere Informationen zum Erstellen und Zugreifen auf Media Foundation Medientypen finden Sie in der Media Foundation SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 




---
description: Arbeiten mit MFT-Medientypen
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Arbeiten mit MFT-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ead31c4291cf41cff62f4341227bf0ee1ad22d12e96a6c9eff87ff5a3e6faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886950"
---
# <a name="working-with-mft-media-types"></a>Arbeiten mit MFT-Medientypen

Ein Medientyp ist eine Möglichkeit, das Format eines Medienstreams zu beschreiben. In Media Foundation werden Medientypen durch die **INTERFACESMediaType-Schnittstelle** dargestellt. Diese Schnittstelle erbt die **INTERFACESAttributes-Schnittstelle.** Die Details eines Medientyps werden als Attribute angegeben.

Um einen neuen Medientyp zu erstellen, rufen Sie die **MFCreateMediaType-Funktion** auf. Diese Funktion gibt einen Zeiger auf die **INTERFACESMediaType-Schnittstelle** zurück. Der Medientyp weist anfänglich keine Attribute auf.

Das Media Foundation SDK bietet mehrere Hilfsfunktionen zum Initialisieren von Medientypen aus Formatstrukturen. Die Funktion **MFInitMediaTypeFromVideoInfoHeader** initialisiert beispielsweise einen Videotyp aus einer **VIDEOINFOHEADER-Struktur,** und die Funktion **MFInitMediaTypeFromWaveFormatEx** initialisiert einen Videotyp aus einer **WAVEFORMATEX-** oder **WAVEFORMATEXTENSIBLE-Struktur.**

Die von den Codecs verwendeten Formattypen sind im Allgemeinen auf die von den **VIDEOINFOHEADER-** und **WAVEFORMATEX-Strukturen** beschriebenen Typen beschränkt.

Weitere Informationen zum Erstellen von und Zugreifen auf Media Foundation Medientypen finden Sie in der Media Foundation SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 




---
title: Schlüssel und Schlüssel-ID
description: Schlüssel und Schlüssel-ID
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), Schlüssel
- DRM (Digital Rights Management), Schlüssel
- Digital Rights Management (DRM), Kid
- DRM (Digital Rights Management), Kid
- Schlüssel-ID (Kid)
- Kid (Schlüssel-ID)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341445"
---
# <a name="key-and-key-id"></a>Schlüssel und Schlüssel-ID

Wenn Sie eine Datei packen, verwenden Sie einen Schlüssel. Ein Schlüssel ist ein Datenelement, das in den Verschlüsselungsalgorithmen verwendet wird, mit denen der Inhalt geschützt wird. Jeder Schlüssel besteht aus zwei Teilen: einem Ausgangswert für den Lizenzschlüssel und einer Schlüssel-ID (häufig als "Kid" abgekürzt). Die Schlüssel-ID ist öffentlich und wird im Dateiheader gespeichert, um den Schlüssel zu identifizieren, der zum Entschlüsseln der Datei erforderlich ist. Der Ausgangswert für den Lizenzschlüssel ist ein geheimer Wert, der vom Content Packager und vom Lizenz Aussteller gemeinsam genutzt werden muss.

Eine Schlüssel-ID identifiziert geschützte Inhalte aus der Perspektive der Lizenz. Sie können zwar dieselbe Schlüssel-ID für mehrere Dateien verwenden, es wird jedoch empfohlen, für jeden geschützten Inhalt stets eine eindeutige Schlüssel-ID zu verwenden.

Viele der in dieser Dokumentation beschriebenen Methoden verwenden Schlüssel-ID-Zeichen folgen, um Lizenzen auszuwählen. Diese Zeichen folgen enthalten die in Base64 codierte Schlüssel-ID.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](drmconcepts.md)
</dt> </dl>

 

 





---
title: Schlüssel und Schlüssel-ID
description: Schlüssel und Schlüssel-ID
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Medienformat-SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), Schlüssel
- DRM (Digital Rights Management), Schlüssel
- Digital Rights Management (DRM), KID
- DRM (Digital Rights Management), KID
- Key ID (KID)
- KID (Schlüssel-ID)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae448cd0c973ad11b55df6365039240ebe2c6ebadb3eda5f70b7f8dd1bfbfbc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929960"
---
# <a name="key-and-key-id"></a>Schlüssel und Schlüssel-ID

Wenn Sie eine Datei packen, verwenden Sie einen Schlüssel. Ein Schlüssel ist ein Teil der Daten, die in den Verschlüsselungsalgorithmen verwendet werden, die den Inhalt schützen. Jeder Schlüssel besteht aus zwei Teilen: einem Lizenzschlüssel-Ausgangswert und einer Schlüssel-ID (häufig als KID abgekürzt). Die Schlüssel-ID ist öffentlich und wird im Dateiheader gespeichert, um den Schlüssel zu identifizieren, der zum Entschlüsseln der Datei erforderlich ist. Der Startwert des Lizenzschlüssels ist ein Geheimniswert, der vom Inhaltspaketgeber und dem Lizenzaussteller freigegeben werden muss.

Eine Schlüssel-ID identifiziert geschützte Inhalte aus der Perspektive der Lizenz. Obwohl Sie dieselbe Schlüssel-ID für mehrere Dateien verwenden können, wird empfohlen, für jeden geschützten Inhalt immer eine eindeutige Schlüssel-ID zu verwenden.

Viele der in dieser Dokumentation beschriebenen Methoden verwenden Schlüssel-ID-Zeichenfolgen, um Lizenzen auszuwählen. Diese Zeichenfolgen enthalten die in Base64 codierte Schlüssel-ID.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](drmconcepts.md)
</dt> </dl>

 

 





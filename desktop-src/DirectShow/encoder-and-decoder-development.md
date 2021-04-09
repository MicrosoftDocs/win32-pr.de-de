---
description: Encoder-und decoderentwicklung
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Encoder-und decoderentwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124555"
---
# <a name="encoder-and-decoder-development"></a>Encoder-und decoderentwicklung

Dieser Abschnitt enthält Artikel zur Entwicklung von Encodern und Decodern für DirectShow. Diese Themen sind für Anwendungsentwickler nicht relevant.

Ein Software Decoder, der die DirectX-Video Beschleunigung (VA) unterstützt, muss als DirectShow-Kopier Transformations Filter implementiert werden. Wenn der Decoder DirectX VA nicht unterstützt, kann er auch als DirectX-Medienobjekt (DMO) implementiert werden. Ein Decoder, der eine Verbindung mit einem Videorenderer herstellt, sollte nicht als ein transdirektionale Filter implementiert werden, da dies zu einer erheblichen Leistungsminderung führt. Informationen zum Schreiben eines Filters für die Kopier Transformation finden Sie unter [Schreiben von Transformations Filtern](writing-transform-filters.md).

Software Encoder können entweder als Transformations Filter oder als DMOS implementiert werden. Encoder verwenden nicht DirectX VA, da DirectX VA derzeit nur für die Komprimierung verwendet wird. Die in diesem Abschnitt beschriebene Encoder-API-Spezifikation ist für Hardware-und Software Encoder relevant.

Dieser Abschnitt enthält die folgenden Themen:

-   [Encoder-API](encoder-api.md)
-   [Decoder-Schnittstellen und Spezifikationen](decoder-interfaces-and-specifications.md)
-   [Decodereinstellungen für Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VMR für DirectShow-Filter Entwickler](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 




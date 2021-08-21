---
description: Encoder- und Decoderentwicklung
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Encoder- und Decoderentwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619225f5d4df9596523724259eb4eee1a9b3bb4c978a3fc400156bc9ee56a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015818"
---
# <a name="encoder-and-decoder-development"></a>Encoder- und Decoderentwicklung

Dieser Abschnitt enthält Artikel zur Entwicklung von Encodern und Decodern für DirectShow. Diese Themen sind für Anwendungsentwickler nicht relevant.

Ein Softwaredecoder, der die DirectX-Videobeschleunigung (DirectX Video Acceleration, VA) unterstützt, muss als DirectShow-Kopiertransformationsfilter implementiert werden. Wenn der Decoder DirectX VA nicht unterstützt, kann er auch als DirectX Media Object (DMO. Ein Decoder, der eine Verbindung mit einem Videorenderer herstellt, sollte nicht als trans-in-place-Filter implementiert werden, da dies zu einer erheblichen Leistungsbeeinträchtigung führt. Informationen zum Schreiben eines Kopiertransformationsfilters finden Sie unter [Schreiben von Transformationsfiltern.](writing-transform-filters.md)

Softwareencoder können entweder als Transformationsfilter oder als DMOs implementiert werden. Encoder verwenden directX VA nicht, da DirectX VA derzeit nur für die Dekomprimierung verwendet wird. Die in diesem Abschnitt beschriebene Encoder-API-Spezifikation ist sowohl für Hardware- als auch für Softwareencoder relevant.

Dieser Abschnitt enthält die folgenden Themen:

-   [Encoder-API](encoder-api.md)
-   [Decoderschnittstellen und Spezifikationen](decoder-interfaces-and-specifications.md)
-   [Decoder Einstellungen für Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VMR für DirectShow-Filterentwickler](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 




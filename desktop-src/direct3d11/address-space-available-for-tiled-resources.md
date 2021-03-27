---
title: Für Kachel Ressourcen verfügbarer Adressraum
description: In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für Kachel Ressourcen verfügbar ist.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719326"
---
# <a name="address-space-available-for-tiled-resources"></a>Für Kachel Ressourcen verfügbarer Adressraum

In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für Kachel Ressourcen verfügbar ist.

Bei 64-Bit-Betriebssystemen sind mindestens 40 Bits des virtuellen Adressraums (1 Terabyte) verfügbar.

Bei 32-Bit-Betriebssystemen ist der Adressraum 32 Bit (4 GB). Bei 32-Bit-ARM-Systemen kann die Erstellung einzelner kachelter Ressourcen fehlschlagen, wenn die Zuordnung mehr als 27 Bits des Adressraums (128 MB) verwenden würde. Dies umfasst alle ausgeblendeten Auffüll Flächen im Adressraum, die die Hardware für Mipmaps, gepackte Kachel Auffüll Zeichen und ggf. das Auffüllen von Oberflächen Dimensionen auf die Potenzen von 2 verwendet.

Auf Grafiksystemen mit einer separaten Seiten Tabelle für die Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) steht der größte Teil dieses Adressraums für GPU-Ressourcen zur Verfügung, die von der Anwendung erstellt werden, obwohl die GPU-Belegungen des Anzeige Treibers in denselben Bereich passen.

In zukünftigen Systemen mit einer Seiten Tabelle, die von der CPU und GPU gemeinsam genutzt wird, wird der verfügbare Adressraum zwischen allen CPU-und GPU-Belegungen in einem Prozess gemeinsam genutzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parameter für die Kachel Ressourcen Erstellung](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 





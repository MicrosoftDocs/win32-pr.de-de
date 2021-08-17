---
title: Verfügbarer Adressraum für gekachelte Ressourcen
description: In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für gekachelte Ressourcen verfügbar ist.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5753fdb9d700689c6ebfffdae4368399c0e4bb36d328c9ff1a8cfc284005214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734282"
---
# <a name="address-space-available-for-tiled-resources"></a>Verfügbarer Adressraum für gekachelte Ressourcen

In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für gekachelte Ressourcen verfügbar ist.

Unter 64-Bit-Betriebssystemen sind mindestens 40 Bit virtueller Adressraum (1 Terabyte) verfügbar.

Bei 32-Bit-Betriebssystemen beträgt der Adressraum 32 Bit (4 GB). Bei 32-Bit-ARM-Systemen kann die Erstellung einzelner gekachelter Ressourcen fehlschlagen, wenn die Zuordnung mehr als 27 Bit Adressraum (128 MB) verwenden würde. Dies schließt alle ausgeblendeten Auffüllungen im Adressraum ein, die die Hardware für Mipmaps, gepackte Kachelauffüllungen und möglicherweise auffüllende Oberflächendimensionen für Potenzen von 2 verwenden kann.

Auf Grafiksystemen mit einer separaten Seitentabelle für die Grafikverarbeitungseinheit (GRAPHICS PROCESSING Unit, GPU) ist der größte Teil dieses Adressraums für GPU-Ressourcen verfügbar, die von der Anwendung erstellt werden, obwohl die vom Anzeigetreiber vorgenommenen GPU-Zuordnungen in den gleichen Bereich passen.

Auf zukünftigen Systemen mit einer von CPU und GPU gemeinsam genutzten Seitentabelle wird der verfügbare Adressraum für alle CPU- und GPU-Zuordnungen in einem Prozess freigegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parameter für die Erstellung von Gekachelten Ressourcen](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 





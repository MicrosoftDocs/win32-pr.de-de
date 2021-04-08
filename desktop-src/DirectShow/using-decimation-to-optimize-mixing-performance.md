---
description: Verwenden von decimations zur Optimierung der Mischungs Leistung
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Verwenden von decimations zur Optimierung der Mischungs Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866459"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Verwenden von decimations zur Optimierung der Mischungs Leistung

> [!IMPORTANT]
> Die in diesem Abschnitt beschriebene Optimierung hängt stark von der zugrunde liegenden Hardware ab. Wenn Sie nicht garantieren können, welche Art von Grafikhardware mit der Anwendung verwendet wird, kann die Darstellung des Video Bilds erheblich beeinträchtigen.

 

Für den Prozessor ist eine hohe Verarbeitungsleistung erforderlich, die auf neueren Systemen größtenteils von der Grafikkarte bereitgestellt wird. Auch wenn die Grafikkarte und der Decoder Auflösungen von 1920 x 1080 unterstützen können, ist der Benutzer möglicherweise nicht immer auf diese Lösung festgelegt. In diesem Fall ist der Grafikchip erforderlich, um ein 1920 x 1080-Abbild zu erstellen und dann die Auflösung zu verringern, bevor es an den Frame Puffer gesendet wird.

Da dies eine Verschwendung der Verarbeitungsleistung darstellt, bietet VMR eine Möglichkeit, das Bild zu dem Zeitpunkt zu dezimieren (zu verringern), zu dem es auf der DirectDraw-Oberfläche gerendert wird. Dadurch entfällt die zusätzliche Speicher Kopie, die erforderlich ist, wenn die Größe des Abbilds geändert werden muss, nachdem es gerendert wurde.

**VMR-7:** Um die Dezimaltrennzeichen zu aktivieren, rufen Sie [**ivmrmixercontrol:: setmixingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) mit dem mixerpref \_ decimateoutput-Flag auf.

**VMR-9:** Um Decimation zu aktivieren, rufen Sie [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ decimateoutput-Flag auf.

Die **setmixingprefs** -Methode muss aufgerufen werden, bevor die VMR verbunden ist. Die Mischungs Einstellungs Flags können nicht geändert werden, sobald das Diagramm ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




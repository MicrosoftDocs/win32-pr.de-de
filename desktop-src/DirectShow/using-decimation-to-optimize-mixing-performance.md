---
description: Verwenden von Dezimation zum Optimieren der Mischen-Leistung
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Verwenden von Dezimation zum Optimieren der Mischen-Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2218566ab31d159f6d0ab74320aa45eb5780bdc3de151de8a7c642016441bacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049619"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Verwenden von Dezimation zum Optimieren der Mischen-Leistung

> [!IMPORTANT]
> Die in diesem Abschnitt beschriebene Optimierung hängt stark von der zugrunde liegenden Hardware ab. Sofern Sie nicht garantieren können, welche Art von Grafikhardware mit der Anwendung verwendet wird, kann dies die Darstellung des Videobilds erheblich herabsetzen.

 

FÜR DIE VERARBEITUNG ist viel Verarbeitungsleistung erforderlich, die auf neueren Systemen größtenteils von der Grafikkarte bereitgestellt wird. Auch wenn die Grafikkarte und der Decoder Auflösungen von 1920 x 1080 unterstützen können, ist der Monitor des Benutzers möglicherweise nicht immer auf diese Auflösung festgelegt. In diesem Fall ist der Grafikchip erforderlich, um ein 1920 x 1080-Bild zu erstellen und dann die Auflösung vor dem Senden an den Framepuffer zu reduzieren.

Da dies eine Verschwendung von Verarbeitungsleistung ist, bietet die VMR eine Möglichkeit, das Bild zu dem Zeitpunkt, zu dem es auf der DirectDraw-Oberfläche gerendert wird, zu dezimieren (reduzieren). Dadurch entfällt die zusätzliche Arbeitsspeicherkopie, die erforderlich ist, wenn die Größe des Bilds nach dem Rendern geändert werden muss.

**VMR-7:** Um die Dezimierung zu aktivieren, rufen Sie [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) mit dem MixerPref \_ DecimateOutput-Flag auf.

**VMR-9:** Um die Dezimierung zu aktivieren, rufen Sie [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ DecimateOutput-Flag auf.

Die **SetMixingPrefs-Methode** muss aufgerufen werden, bevor die VMR verbunden wird. Die Gemischtpräferenzflags können nicht geändert werden, sobald das Diagramm ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Gemischtmodus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




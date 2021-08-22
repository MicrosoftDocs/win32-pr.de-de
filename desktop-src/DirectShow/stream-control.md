---
description: Stream-Steuerelement
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Stream-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8da9f317137904a87356bbdcc10dc68357513cf168a0b7b7ea46398ed47a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072384"
---
# <a name="stream-control"></a>Stream-Steuerelement

Die [**IVMRVideoStreamControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) für die Eingabepins des virtuellen Computers ermöglicht Anwendungen und Upstreamfiltern, das Verhalten der Mixerkomponente zu steuern, einschließlich der Z-Reihenfolge und des aktiven Zustands der VMR-Eingabestreams. Obwohl diese Schnittstelle an den Stecknadeln verfügbar gemacht wird, wird sie auf der Mixerkomponente des virtuellen Computers ausgeführt, sodass sie nur verfügbar ist, wenn der Mixer geladen wird. Dies ist der Fall, wenn die VMR mehrere Eingabestreams verarbeitet. Upstreamfilter verwenden die [**Methoden SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) und [**GetColorKey,**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) um den Quellcode zu steuern. Diese Methoden ermöglichen Effekte wie die Überlagerung von Animation über Video. Legen Sie einfach den Farbschlüssel auf die Hintergrundfarbe des Animationsstreams fest, und der VMR mischen diesen Stream mit einem anderen Videostream. Anwendungen sollten darauf achten, den Farbschlüssel nicht in einen Wert zu ändern, der sich von dem Wert absetzt, der von einem Upstreamfilter wie einem Decoder verwendet wird.

Filter verwenden die [**Methoden GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) und [**SetStreamActiveState,**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) um dem Mixer anzugeben, ob Eingabedaten von einem angegebenen Pin erwartet werden. Beispielsweise verwendet der Line21-Decoder diese Methoden, um den VMR-Eingabepin für Line21-Daten nur dann zu aktivieren, wenn diese Daten im Stream vorhanden sind. Das Festlegen eines Pins auf einen inaktiven Zustand weist den Mixer an, nicht auf Daten von einem angegebenen Pin zu warten, bevor er das Bild zusammenordnet.

 

 




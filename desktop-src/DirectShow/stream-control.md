---
description: Stream-Steuerelement
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Stream-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866475"
---
# <a name="stream-control"></a>Stream-Steuerelement

Die [**ivmrvideostreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) -Schnittstelle in den eingabepin (s) des VMR ermöglicht Anwendungen und upstreamfiltern, das Verhalten der Mischungs Komponente zu steuern, einschließlich der Z-Reihenfolge und des aktiven Zustands der Eingabestreams von VMR. Obwohl diese Schnittstelle auf den Pins verfügbar gemacht wird, wird Sie mit der Mischungs Komponente von VMR betrieben, sodass Sie nur verfügbar ist, wenn der Mixer geladen wird. Dies ist der Fall, wenn der VMR mehrere Eingabedaten Ströme verarbeitet. Upstreamfilter verwenden die Methoden [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) und [**getcolorkey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) , um den Quell Farben Schlüssel zu steuern. Diese Methoden ermöglichen Effekte, wie z. b. das Überlagern der Animation über Video. Legen Sie einfach den Farbschlüssel auf die Hintergrundfarbe des Animations Streams fest, und der VMR vermischt diesen Stream mit einem anderen Videostream. Anwendungen sollten darauf achten, den Farbschlüssel nicht in einen anderen Wert als den Wert zu ändern, der von einem upstreamfilter verwendet wird, z. b. ein Decoder.

Filter verwenden die [**getstreamactivestate**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) -Methode und die [**setstreamactivestate**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) -Methode, um dem Mixer mitzuteilen, ob die Eingabedaten von einer angegebenen Pin erwartet werden. Beispielsweise verwendet der Line21-Decoder diese Methoden, um die VMR-Eingabe-PIN für Line21-Daten nur dann zu aktivieren, wenn diese Daten im Stream vorhanden sind. Das Festlegen einer PIN auf einen inaktiven Status weist den Mixer an, vor der Zusammensetzung des Bilds nicht auf Daten von einer angegebenen PIN zu warten.

 

 




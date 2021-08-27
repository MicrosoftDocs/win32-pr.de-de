---
title: Dynamische Pufferserialisierung
description: Bei Verwendung des dynamischen Pufferstils der Serialisierung wird der Marshallingpuffer vom Stub zugeordnet, und die Daten werden in diesen Puffer codiert und an Sie übergeben. Beim Unmarshaling geben Sie den Puffer an, der die Daten enthält.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea47a87a9d2e566dcfb033b0c9e9403ae72081afe0a1554337dbacfef9c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021680"
---
# <a name="dynamic-buffer-serialization"></a>Dynamische Pufferserialisierung

Bei Verwendung des dynamischen Pufferstils der Serialisierung wird der Marshallingpuffer vom Stub zugeordnet, und die Daten werden in diesen Puffer codiert und an Sie übergeben. Beim Unmarshaling geben Sie den Puffer an, der die Daten enthält.

Der dynamische Pufferstil der Serialisierung verwendet die folgenden Routinen:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Die [**MesEncodeDynBufferHandleCreate-Funktion**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) weist den für das Codierungshandle benötigten Arbeitsspeicher zu und initialisiert ihn anschließend. Die Anwendung kann [**MesBufferHandleReset aufrufen,**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) um das Handle erneut zu initialisieren. Sie ruft [**MesHandleFree auf,**](/windows/desktop/api/Midles/nf-midles-meshandlefree) um den Arbeitsspeicher des Handles frei zu geben. Verwenden Sie [**MesDecodeBufferHandleCreate,**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)um ein Decodierungshandle zu erstellen, das dem dynamischen Puffercodierungshandle entspricht.

 

 





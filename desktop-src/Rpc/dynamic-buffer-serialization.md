---
title: Dynamische pufferserialisierung
description: Bei Verwendung der dynamischen Pufferart der Serialisierung wird der marshallingpuffer vom Stub zugeordnet, und die Daten werden in diesen Puffer codiert und an Sie zurückgegeben. Wenn Sie das Marshalling durchlaufen, stellen Sie den Puffer bereit, der die Daten enthält.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471260"
---
# <a name="dynamic-buffer-serialization"></a>Dynamische pufferserialisierung

Bei Verwendung der dynamischen Pufferart der Serialisierung wird der marshallingpuffer vom Stub zugeordnet, und die Daten werden in diesen Puffer codiert und an Sie zurückgegeben. Wenn Sie das Marshalling durchlaufen, stellen Sie den Puffer bereit, der die Daten enthält.

Der dynamische pufferstil der Serialisierung verwendet die folgenden Routinen:

-   [**Mesencoentdynbufferlenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**Mesdecodebufferlagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**Mesbufferhandlereset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**Meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Die [**mesencodebug**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) -Funktion ordnet den für das Codierungs handle benötigten Arbeitsspeicher zu und initialisiert Sie dann. Die Anwendung kann [**mesbufferhandlereset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) aufrufen, um das Handle erneut zu initialisieren. Sie ruft [**meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree) auf, um den Arbeitsspeicher des Handles freizugeben. Zum Erstellen eines Decodierungs Handles, das dem dynamischen Puffer Codierungs Handle entspricht, verwenden Sie [**mesdecodebufferlenker Create**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 





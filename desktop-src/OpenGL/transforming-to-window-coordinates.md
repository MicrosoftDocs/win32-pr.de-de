---
title: Transformieren in Fensterkoordinaten
description: Bevor Clipkoordinaten in Fensterkoordinaten konvertiert werden, werden sie durch den Wert von w geteilt, um normalisierte Gerätekoordinaten zu erhalten.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- OpenGL-Verarbeitungspipeline, Konvertieren in Fensterkoordinaten
- Konvertieren in Fensterkoordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa74b42457349b14e151099a3c4238e855ad0001e1b8f9416808a1279b82345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887990"
---
# <a name="transforming-to-window-coordinates"></a>Transformieren in Fensterkoordinaten

Bevor Clipkoordinaten in Fensterkoordinaten konvertiert werden, werden sie durch den Wert *von w* geteilt, um normalisierte Gerätekoordinaten zu erhalten. Die Auf diese normalisierten Koordinaten angewendete Viewporttransformation erzeugt Fensterkoordinaten. Sie steuern den Viewport, der den Bereich des Bildschirmfensters bestimmt, in dem ein Bild angezeigt wird, mit [**glDepthRange**](gldepthrange.md) und [**glViewport.**](glviewport.md)

 

 





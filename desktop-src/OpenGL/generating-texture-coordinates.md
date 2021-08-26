---
title: Generieren von Texturkoordinaten
description: Anstatt Texturkoordinaten explizit zu liefern, können Sie OpenGL diese als Funktion anderer Scheitelpunktdaten mit glTexGen\ generieren lassen.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- OpenGL-Verarbeitungspipeline, Texturkoordinaten
- Texturkoordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e7b6bc2d1263fac046f2d3078e2bab9bf8a789cacb335137ba27443b12b89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082280"
---
# <a name="generating-texture-coordinates"></a>Generieren von Texturkoordinaten

Anstatt Texturkoordinaten explizit zu liefern, können Sie OpenGL diese als Funktion anderer Scheitelpunktdaten mit [glTexGen \* generieren lassen.](gltexgen-functions.md) Nachdem die Texturkoordinaten angegeben oder generiert wurden, werden sie von der Texturmatrix transformiert. Diese Matrix wird mit den gleichen Funktionen gesteuert, die auch für Matrixtransformationen verwendet werden (siehe [Matrixtransformationen](matrix-transformations.md)).

 

 





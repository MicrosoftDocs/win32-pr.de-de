---
title: Auswahl
description: Auswahl gibt den aktuellen Inhalt des Namens Stapels zurück, bei dem es sich um ein Array von Namen mit ganzzahligen Werten handelt.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- Auswahlmodus OpenGL
- Auswahl Treffer OpenGL
- Treffer Datensätze OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310376"
---
# <a name="selection"></a>Auswahl

Auswahl gibt den aktuellen Inhalt des Namens Stapels zurück, bei dem es sich um ein Array von Namen mit ganzzahligen Werten handelt. Sie weisen die Namen zu und erstellen den namens Stapel innerhalb des Modellierungs Codes, der die Geometrie von Objekten angibt, die Sie zeichnen möchten. Wenn dann im Auswahlmodus ein primitiv das Clip Volume überschneidet, tritt ein Auswahl Treffer auf. Der Treffer Daten Satz, der in das Auswahl Array geschrieben wird, das Sie mit [**glselectbuffer**](glselectbuffer.md)angegeben haben, enthält Informationen zum Inhalt des Namens Stapels zum Zeitpunkt des Treffer.

> [!Note]  
> Nennen Sie [**glselectbuffer**](glselectbuffer.md) , bevor Sie OpenGL mit [**glrendermode**](glrendermode.md)in den Auswahlmodus versetzen. Es ist nicht garantiert, dass der gesamte Inhalt des Namens Stapels zurückgegeben wird, bis Sie **glrendermode** aufgerufen haben, um OpenGL aus dem Auswahlmodus zu nehmen.

 

Ändern Sie den Namen Stapel mit " [**glinitnames**](glinitnames.md)", " [**glloadname**](glloadname.md)", " [**glpushname**](glpushname.md)" und " [**glpopname**](glpopname.md)". Sie können auch " [**glupickmatrix**](glupickmatrix.md) " zur Auswahl verwenden.

 

 





---
title: Schalt Flächentyp
description: Schalt Flächentyp
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Typen
- Skins, Schaltflächen Typen
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855683"
---
# <a name="button-type"></a>Schalt Flächentyp

Schaltflächen verfügen über zwei allgemeine Typen: "Location" und "Region". Jeder allgemeine Typ verfügt über drei bestimmte Typen, die jeweils sechs Schaltflächen Typen erstellen.

> [!Note]  
> Schaltflächen Typen sind in Skins für Windows Media Player 10 Mobile oder höher veraltet.

 

Location-Schaltflächen Typen

Standort Schaltflächen verwenden Koordinaten, um Ihre Positionen relativ zum Hintergrund zu definieren. In der folgenden Tabelle sind die Werte aufgeführt, die für Speicherort-Schaltflächen Typen gültig sind. Sie müssen keine Werte für Typen definieren, die in der Skin nicht verwendet werden.



| Wert  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Push   | Definiert eine Schaltfläche, die ein Ereignis einmal auslöst. Die Schaltfläche muss jedes Mal pusht werden, um weitere Ereignisse zu initiieren. Ein Beispiel wäre eine Schaltfläche, die zum nächsten Element in der Wiedergabeliste wechselt. Der Speicherort der Schaltfläche wird durch seine Koordinaten definiert.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ein-/Ausschalten | Definiert eine Schaltfläche, die ein Ereignis auslöst, das einen Zustand ändert. Der Status bleibt bestehen, bis die Schaltfläche erneut verschoben wird. Ein Beispiel ist eine Schaltfläche, mit der die Wiedergabeliste heruntergefahren wird. Wenn sich die Wiedergabeliste in einem gemischten Zustand befindet, bleibt Sie gemischt, bis die Schaltfläche erneut verschoben wird. Der Speicherort der Schaltfläche wird durch seine Koordinaten definiert.                                                                                                                                                                                                                                                                                                                                                           |
| 2push  | Definiert eine Schaltfläche, die ein Ereignis auslöst, und wechselt in einen Zustand, der zum Auslösen eines anderen Ereignisses bereit ist. Die beiden Zustände werden jedes Mal ein-und ausgeschaltet, wenn die Schaltfläche gedrückt wird. Ein Beispiel hierfür ist eine Schaltfläche, die die Funktion **PLAYPAUSE** verwendet, um zwischen Wiedergabe und Anhalten des aktuellen Medien Elements zu wechseln. Wenn die Schaltfläche zum ersten Mal per Pushvorgang übertragen wird, wird der primäre Wiedergabe Zustand ausgelöst und ein sekundäres Bild angezeigt, um anzugeben, dass ein **Pausen** Ereignis ausgelöst werden kann. Wenn die Schaltfläche erneut verschoben wird, wird der Pause-Zustand ausgelöst, und das ursprüngliche Bild wird angezeigt, um anzugeben, dass ein **Wiedergabe** Ereignis ausgelöst werden kann. Der Speicherort der Schaltfläche wird durch seine Koordinaten definiert. |



 

Regions-Schaltflächen Typen

Bereichs Schaltflächen verwenden Farbbereiche im Regions Bild, um zu definieren, wo Abzweigungen für eine bestimmte Schaltfläche verarbeitet werden. In der folgenden Tabelle sind die Werte aufgeführt, die für Regions Schaltflächen Typen gültig sind. Sie müssen keine Werte für Typen definieren, die in der Skin nicht verwendet werden.



| Wert     | BESCHREIBUNG                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Pushtreffer   | Vergleichbar mit dem Wert der Push-Schaltfläche, mit dem Unterschied, dass der Trefferbereich der Schaltfläche durch den Farbwert im Bereichs Bild definiert wird.   |
| Ein-und klein Treffer | Ähnlich wie beim Wert der UMSCHALT Fläche, mit der Ausnahme, dass der Trefferbereich der Schaltfläche durch den Farbwert im Bild des Bereichs definiert wird. |
| 2pushhit  | Ähnelt dem 2push-Schaltflächen Wert, mit dem Unterschied, dass der Trefferbereich der Schaltfläche durch den Farbwert im Bereichs Bild definiert wird.  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 





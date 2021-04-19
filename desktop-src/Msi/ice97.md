---
description: ICE97 überprüft, ob zwei Komponenten eine freigegebene Komponente nicht im selben Verzeichnis isolieren.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348684"
---
# <a name="ice97"></a>ICE97

ICE97 überprüft, ob zwei Komponenten eine freigegebene Komponente nicht im selben Verzeichnis isolieren.

## <a name="result"></a>Ergebnis

ICE97 gibt die folgenden Warnungen aus.



| ICE97-Warnung                                                                                                                                                                    | BESCHREIBUNG                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Mit dieser Komponente \[ 1 \] wird die freigegebene Komponente in demselben Verzeichnis \[ 2 \] wie ein anderes installiert, das Komponenten Regeln unterbricht, wenn mindestens eine Komponente für die Installation ausgewählt ist. | Zwei Komponenten dürfen eine freigegebene Komponente nicht in dasselbe Verzeichnis isolieren. |



 

Beispielsweise werden Component1 und Component2, die componentshared gemeinsam verwenden, im gleichen Verzeichnis installiert. Beide geben componentshared als isolierte Komponente an. Aufgrund der Isolierung werden die Dateien in componentshared zweimal in den Verzeichnis \_ Verweis für Component1 und Component2 kopiert. Die Komponenten verfügen jetzt über einen Verweis Zähler für die Kopie der Dateien. Dies verstößt gegen die installerkomponentenregeln. Wenn Component1 deinstalliert wird, werden die Dateien der isolierten Komponenten entfernt, und Component2 ist beschädigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




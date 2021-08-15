---
description: ICE97 überprüft, ob zwei Komponenten eine freigegebene Komponente nicht im gleichen Verzeichnis isolieren.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29575d533e945cef922110315cd3300f56fe62ae61b34c92de7175916e6657ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315240"
---
# <a name="ice97"></a>ICE97

ICE97 überprüft, ob zwei Komponenten eine freigegebene Komponente nicht im gleichen Verzeichnis isolieren.

## <a name="result"></a>Ergebnis

ICE97 gibt die folgenden Warnungen aus.



| ICE97-Warnung                                                                                                                                                                    | BESCHREIBUNG                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Diese Komponente \[ 1 \] installiert die freigegebene Komponente im selben Verzeichnis \[ 2 wie eine \] andere, wodurch Komponentenregeln unterbrochen werden, wenn beide (oder mehrere) Komponenten für die Installation ausgewählt sind. | Zwei Komponenten dürfen eine freigegebene Komponente nicht im gleichen Verzeichnis isolieren. |



 

Beispielsweise werden Component1 und Component2, die ComponentShared gemeinsam nutzen, im gleichen Verzeichnis installiert. Beide geben ComponentShared als isolierte Komponente an. Aufgrund der Isolation werden die Dateien in ComponentShared zweimal in den \_ Verzeichnisverweis für Component1 und Component2 kopiert. Die Komponenten verfügen jetzt über einen Verweiszähler für die Kopie der Dateien. Dies verstößt gegen die Regeln der Installer-Komponente. Wenn Component1 deinstalliert wird, werden die isolierten Komponentendateien entfernt, und Component2 wird beschädigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




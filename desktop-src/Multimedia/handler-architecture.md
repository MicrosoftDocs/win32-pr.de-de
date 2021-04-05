---
title: Handlerarchitektur
description: Handlerarchitektur
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037064"
---
# <a name="handler-architecture"></a>Handlerarchitektur

Die interne Funktion eines Datei-oder streamhandlers wird vom Handler selbst definiert. Für eine Anwendung wird in der Regel ein Datei Handler als Modul zum Lesen und Schreiben von AVI-Dateien angezeigt. Entsprechend wird ein Datenstrom Handler als Modul angezeigt, um einen bestimmten Typ von Datenstrom zu lesen und zu schreiben. Die konsistente Stream-Schnittstelle macht die Quelle und das Ziel des Streams unwichtig für die Anwendung, die den Handler verwendet.

Ein Datei Handler ermöglicht den Zugriff auf eine Datenquelle, die aus einem oder mehreren Datenströmen besteht. Datei Handler ermöglichen in der Regel den Zugriff auf Datenträger Dateien, die einen oder mehrere Datenströme enthalten, und die internen Funktionen des Datei Handler lesen und schreiben die Multimedia-Daten. Datei Handler können jedoch mit jeder beliebigen Datenquelle arbeiten, z. b. einem digitalen Übertragungskanal, der mehrere gemischte Datenströme enthält.

Im Gegensatz dazu verarbeitet ein Datenstrom Handler einen Datentyp und wird als Datenstrom zu einer Anwendung angezeigt. Ein Datenstrom Handler kann Daten bereitstellen, die er herstellt, oder er kann Daten aus einer Datei oder einer externen Quelle abrufen. Die Daten werden in einem Format bereitstellt, das von der Anwendung verwendet werden kann.

 

 





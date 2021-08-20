---
title: Handlerarchitektur
description: Handlerarchitektur
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0da7846f31c94202d8d50ac0566c87ef5db085a0b9efb3f9250468346512db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141093"
---
# <a name="handler-architecture"></a>Handlerarchitektur

Die interne Funktion eines Datei- oder Streamhandlers wird vom Handler selbst definiert. Für eine Anwendung wird ein Dateihandler in der Regel als Modul zum Lesen und Schreiben von AVI-Dateien angezeigt. Ebenso wird ein Streamhandler als Modul zum Lesen und Schreiben eines bestimmten Datenstromtyps angezeigt. Die konsistente Streamschnittstelle macht die Quelle und das Ziel des Streams für die Anwendung, die den Handler verwendet, unwichtig.

Ein Dateihandler ermöglicht den Zugriff auf eine Datenquelle, die aus einem oder mehreren Datenströmen besteht. Dateihandler bieten in der Regel Zugriff auf Datenträgerdateien, die einen oder mehrere Datenströme enthalten, und die internen Funktionen des Dateihandlers lesen und schreiben die Multimediadaten. Dateihandler können jedoch mit jeder Datenquelle arbeiten, z. B. mit einem digitalen Übertragungskanal, der mehrere unbestimmte Datenströme enthält.

Im Gegensatz dazu verarbeitet ein Streamhandler einen Datentyp und wird als Datenstrom für eine Anwendung angezeigt. Ein Streamhandler kann Daten bereitstellen, die er herstellt, oder Daten aus einer Datei oder einer externen Quelle abrufen. Die Daten werden in einem Format bereitgestellt, das ihre Anwendung verwenden kann.

 

 





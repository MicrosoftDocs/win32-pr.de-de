---
description: Transformationen mit sicherem vollständigen Pfad müssen über eine Quelle verfügen, die sich unter dem vollständigen Pfad befindet, der in der TRANSFORMS-Eigenschaft angegeben ist.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Sichere Vollständige Pfadtransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f55e16f40d99deceb8b625297cf447ebf5ec7dfb14a25518554804cf35b572e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040900"
---
# <a name="secure-full-path-transforms"></a>Sichere Vollständige Pfadtransformationen

Transformationen mit sicherem vollständigen Pfad müssen über eine Quelle verfügen, die sich unter dem vollständigen Pfad befindet, der in der [**TRANSFORMS-Eigenschaft**](transforms.md) angegeben ist. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen in einem Cache, in dem der Benutzer auf einem sicheren Dateisystem keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, kann der Cache nur mit dem angegebenen Pfad wiederhergestellt werden. Durch das Entfernen eines Produkts durch einen Benutzer werden alle sicheren Transformationen für dieses Produkt vom Computer des Benutzers entfernt.

Um Transformationen mit sicheren vollständigen Pfaden bei der Installation eines Pakets anzuwenden, legen Sie die [TransformsSecure-Richtlinie](transformssecure-policy.md) oder die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) fest, oder übergeben \| Sie das erste Zeichen in der Transformationsliste. Die vollständigen Pfade zur Quelle jeder Transformation müssen in der Transformationszeichenfolge übergeben werden. Wenn relative Pfade in der Liste enthalten sind, schlägt die Installation fehl. Die Transformationsquelle muss nicht mit der Quelle des Pakets gefunden werden.

 

 




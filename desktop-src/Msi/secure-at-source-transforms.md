---
description: Secure-at-Source-Transformationen müssen über eine Quelle verfügen, die sich im Stammverzeichnis der Quelle für das Paket befindet.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Secure-At-Source-Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f591e6f30c11ec9fa7edf2f943ef1f660a0a3b12ff87c3c1de0984328652565b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041000"
---
# <a name="secure-at-source-transforms"></a>Secure-At-Source-Transformationen

Secure-at-Source-Transformationen müssen über eine Quelle verfügen, die sich im Stammverzeichnis der Quelle für das Paket befindet. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen in einem Cache, in dem der Benutzer auf einem sicheren Dateisystem keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode entspricht der Suche in der Quellliste nach einer .msi-Datei. Weitere Informationen finden Sie unter [Quellresilienz.](source-resiliency.md) Durch das Entfernen eines Produkts durch einen Benutzer werden alle sicheren Transformationen für dieses Produkt vom Computer des Benutzers entfernt.

Legen Sie zum Anwenden von Secure-at-Source-Transformationen bei der Installation eines Pakets die [TransformsSecure-Richtlinie](transformssecure-policy.md) oder die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) fest, oder erstellen Sie @ zum ersten Zeichen, das in der Transformationsliste übergeben wird. Jede Transformation muss durch einen Dateinamen angegeben werden und sich im Stammverzeichnis der Quelle für das Paket befinden. Wenn sich eine der Transformationen nicht im Stammverzeichnis der Paketquelle befindet, tritt bei der Installation ein Fehler auf. Weitere Informationen finden Sie unter [Anwenden von Transformationen.](applying-transforms.md)

 

 




---
description: Bei der Transformation für sichere Quellen muss sich eine Quelle im Stammverzeichnis der Quelle für das Paket befinden.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Secure-at-Source-Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869043"
---
# <a name="secure-at-source-transforms"></a>Secure-at-Source-Transformationen

Bei der Transformation für sichere Quellen muss sich eine Quelle im Stammverzeichnis der Quelle für das Paket befinden. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen in einem Cache, in dem der Benutzer in einem sicheren Dateisystem keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht verfügbar ist, sucht der Installer nach einer Quelle, um den Cache wiederherzustellen. Die-Methode ist identisch mit dem Durchsuchen der Quell Liste nach einer MSI-Datei. Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md). Durch das Entfernen eines Produkts durch einen beliebigen Benutzer werden alle sicheren Transformationen für das Produkt auf dem Computer des Benutzers entfernt.

Wenn Sie bei der Installation eines Pakets sichere at-Source-Transformationen anwenden möchten, legen Sie die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft fest, oder geben Sie @ das erste Zeichen an, das in der Transformations Liste übergangen wird. Jede Transformation muss durch einen Dateinamen angegeben werden und muss sich im Stammverzeichnis der Quelle für das Paket befinden. Wenn sich eine der Transformationen nicht im Stammverzeichnis der Paketquelle befindet, tritt bei der Installation ein Fehler auf. Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md).

 

 




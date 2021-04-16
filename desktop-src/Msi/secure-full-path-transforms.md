---
description: Bei Secure-Full-Path-Transformationen muss sich eine Quelle unter dem vollständigen Pfad befinden, der in der Transformationen-Eigenschaft angegeben ist.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Sichere vollständige Pfad Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530302"
---
# <a name="secure-full-path-transforms"></a>Sichere vollständige Pfad Transformationen

Bei Secure-Full-Path-Transformationen muss sich eine Quelle unter dem vollständigen Pfad befinden, der in der [**Transformationen**](transforms.md) -Eigenschaft angegeben ist. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen in einem Cache, in dem der Benutzer in einem sicheren Dateisystem keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht verfügbar ist, kann der Cache nur unter Verwendung des angegebenen Pfads wieder hergestellt werden. Durch das Entfernen eines Produkts durch einen beliebigen Benutzer werden alle sicheren Transformationen für das Produkt auf dem Computer des Benutzers entfernt.

Zum Anwenden von Transformationen für sichere vollständige Pfade bei der Installation eines Pakets legen Sie die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft fest, oder legen Sie \| das erste Zeichen in der Transformations Liste an. Die vollständigen Pfade zur Quelle der einzelnen Transformationen müssen in der Transformations Zeichenfolge übermittelt werden. Wenn in der Liste relative Pfade vorhanden sind, tritt bei der Installation ein Fehler auf. Die Transformations Quelle muss sich nicht mit der Quelle des Pakets befinden.

 

 




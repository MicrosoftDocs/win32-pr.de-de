---
description: Eine Sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei aus, nicht auf die tatsächlich zugeordnete Menge an Speicherplatz.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Sparsedateien und Datenträgerkontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e78e9d35e557585f17df6c4672a04b2997792f95b0fca63d2e6a2345a7a8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015078"
---
# <a name="sparse-files-and-disk-quotas"></a>Sparsedateien und Datenträgerkontingente

Eine Sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei aus, nicht auf die tatsächlich zugeordnete Menge an Speicherplatz. Das heißt, das Erstellen einer 50-MB-Datei mit allen 0 Bytes verbraucht 50 MB des Kontingents dieses Benutzers. Dies bedeutet, dass sich der Benutzer beim Schreiben von Daten in die Sparsedatei keine Gedanken über die Überschreitung seiner harte Kontingentgrenze machen muss, da ihm der Speicherplatz bereits in Rechnung gestellt wurde. Systemadministratoren sollten nicht auf die Größe einer Sparsedatei zählen, die klein bleibt. Daher sollten sie ihren Benutzern keine harte Kontingentgrenze gewähren, die den verfügbaren physischen Speicherplatz trotz der Verwendung von Sparsedateien überschreitet.

 

 




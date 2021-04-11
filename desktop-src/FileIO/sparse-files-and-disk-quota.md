---
description: Eine sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei und nicht die tatsächlich zugeordnete Menge an Speicherplatz aus.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Sparsesdateien und Datenträger Kontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129757"
---
# <a name="sparse-files-and-disk-quotas"></a>Sparsesdateien und Datenträger Kontingente

Eine sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei und nicht die tatsächlich zugeordnete Menge an Speicherplatz aus. Das heißt, dass das Erstellen einer 50-MB-Datei mit allen 0 Bytes 50 MB dieses Benutzer Kontingents beansprucht. Dies bedeutet, dass der Benutzer beim Schreiben von Daten in die sparsedatei keine Gedanken mehr über die Überschreitung seines festen Kontingent Limits machen muss, da ihm bereits der Platz in Rechnung gestellt wurde. System Administratoren sollten nicht die Größe einer kleinen sparsedatei zählen, die kleiner ist. Daher sollten Sie nicht Ihren Benutzern feste Kontingent Limits gewähren, die den verfügbaren physischen Speicherplatz überschreiten, trotz der Verwendung von Dateien mit geringer Dichte.

 

 




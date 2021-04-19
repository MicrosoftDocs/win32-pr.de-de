---
description: Beschreibt ein Scatter-Gather-Schema zum Lesen oder Schreiben von nicht zusammenhängenden Datenblöcken in einem Vorgang.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lesen aus oder schreiben in Dateien mit einem Scatter-Gather Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360720"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lesen aus oder schreiben in Dateien mit einem Scatter-Gather Schema

Ein Scatter-Gather-Schema verwendet das Betriebssystem, um mehrere diskrete Datenblöcke (z. b. Datenbankeinträge) aus einer Datei in getrennte, nicht zusammenhängende Puffer im Arbeitsspeicher zu übermitteln. Ein Scatter-Gather-Schema schreibt auch die Daten aus nicht zusammenhängenden Puffern in einem Vorgang.

Eine Anwendung kann ein Scatter-Gather-Schema implementieren, indem die Funktionen " [**leserfilescatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) " und " [**Write filegather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) " verwendet werden.

 

 




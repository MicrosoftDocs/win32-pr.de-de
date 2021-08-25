---
description: Beschreibt ein Punktdiagrammschema zum Lesen oder Schreiben nicht zusammenhängender Datenblöcke in einem Vorgang.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lesen aus oder Schreiben in Dateien mithilfe eines Scatter-Gather Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc8a7ee9fcae2a54ac31c51a7c038e3d9442a6ccded2fc7dab916c7a6165a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914480"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lesen aus oder Schreiben in Dateien mithilfe eines Scatter-Gather Schemas

Ein Punktdiagrammschema verwendet das Betriebssystem, um in einem Vorgang mehrere diskrete Datenblöcke (z. B. Datenbankdatensätze) aus einer Datei bereitzustellen, um nicht zusammenhängende Puffer im Arbeitsspeicher zu trennen. Ein Punktdiagrammschema schreibt die Daten auch aus nicht zusammenhängenden Puffern in einem Vorgang.

Eine Anwendung kann ein Punktdiagrammschema implementieren, indem die [**Funktionen ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) und [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) verwendet werden.

 

 




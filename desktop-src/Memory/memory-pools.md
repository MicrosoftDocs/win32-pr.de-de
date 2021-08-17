---
description: 'Der Arbeitsspeicher-Manager erstellt die folgenden Speicherpools, die das System verwendet, um Arbeitsspeicher zu reservieren: nicht auspager Pool und Auspagepool.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Speicherpools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a49597cf90324395c50a4e44aac03815426f0c1de8ea2c7ca7aa85b5cdac95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808997"
---
# <a name="memory-pools"></a>Speicherpools

Der Arbeitsspeicher-Manager erstellt die folgenden Speicherpools, die das System verwendet, um Arbeitsspeicher zu reservieren: nicht auspager Pool und Auspagepool. Beide Speicherpools befinden sich in der Region des Adressraums, der für das System reserviert ist und dem virtuellen Adressraum jedes Prozesses zugeordnet ist. Der nicht auspagete Pool besteht aus virtuellen Speicheradressen, die sich garantiert im physischen Speicher befinden, solange die entsprechenden Kernelobjekte zugeordnet werden. Der aus paged-Pool besteht aus virtuellem Arbeitsspeicher, der in das System und aus dem System aus- und auspaget werden kann. Zur Verbesserung der Leistung verfügen Systeme mit einem einzelnen Prozessor über drei Auspagepools, und Multiprozessorsysteme verfügen über fünf Auspagepools.

Die Handles für [Kernelobjekte werden](../sysinfo/kernel-objects.md) im ausgelagerten Pool gespeichert, sodass die Anzahl der Handles, die Sie erstellen können, auf dem verfügbaren Arbeitsspeicher basiert.

Das System zeichnet die Grenzwerte und aktuellen Werte für den nicht auspageierten Pool, den auspageierten Pool und die Nutzung der Seitendatei auf. Weitere Informationen finden Sie unter [Arbeitsspeicherleistungsinformationen.](memory-performance-information.md)

 

 

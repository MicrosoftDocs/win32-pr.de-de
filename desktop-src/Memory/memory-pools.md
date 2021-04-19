---
description: 'Der Speicher-Manager erstellt die folgenden Speicherpools, die das System verwendet, um Speicher zuzuweisen: nicht Auslagerungs Pool und Auslagerungs Pool.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Speicher Pools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357096"
---
# <a name="memory-pools"></a>Speicher Pools

Der Speicher-Manager erstellt die folgenden Speicherpools, die das System verwendet, um Speicher zuzuweisen: nicht Auslagerungs Pool und Auslagerungs Pool. Beide Speicherpools befinden sich in der Region des Adressraums, der für das System reserviert ist und dem virtuellen Adressraum der einzelnen Prozesse zugeordnet ist. Der nicht-Auslagerungs Pool besteht aus virtuellen Speicheradressen, die sich garantiert im physischen Speicher befinden, solange die entsprechenden Kernel Objekte zugewiesen werden. Der Auslagerungs Pool besteht aus virtuellem Arbeitsspeicher, der ein-und auslagern aus dem System möglich ist. Um die Leistung zu verbessern, verfügen Systeme mit einem einzelnen Prozessor über drei auslagerbare Pools, und Multiprozessorsysteme verfügen über fünf auslagerbare Pools.

Die Handles für [Kernel Objekte](../sysinfo/kernel-objects.md) werden im ausgelagerten Pool gespeichert, sodass die Anzahl der Handles, die Sie erstellen können, auf dem verfügbaren Arbeitsspeicher basiert.

Das System zeichnet die Limits und die aktuellen Werte für den nicht auslagerten Pool, den Auslagerungs Pool und die Auslagerungs Datei Verwendung auf. Weitere Informationen finden Sie unter [Informationen zur Speicherleistung](memory-performance-information.md).

 

 

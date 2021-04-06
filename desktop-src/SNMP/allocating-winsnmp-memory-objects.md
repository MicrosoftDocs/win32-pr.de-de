---
title: Zuordnen von WinSNMP-Speicher Objekten
description: Deskriptoren, Ressourcen Handles und Zeichen folgen im C-Stil sind die drei Typen von Speicher Objekten in der WinSNMP-Programmierumgebung.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036288"
---
# <a name="allocating-winsnmp-memory-objects"></a>Zuordnen von WinSNMP-Speicher Objekten

Deskriptoren, Ressourcen Handles und Zeichen folgen im C-Stil sind die drei Typen von Speicher Objekten in der WinSNMP-Programmierumgebung.

Der Objekttyp bestimmt, ob die Microsoft WinSNMP-Implementierung oder die WinSNMP-Anwendung den Speicher für das-Objekt zuordnet und zuordnet. Dadurch wird die unnötige Zuordnung von temporären Pufferspeicher und unnötigem Kopieren von Puffern reduziert.

In der folgenden Tabelle werden die Zuordnung und Freigabe von Ressourcen für WinSNMP-Speicher Objekte zusammengefasst.



| Objekttyp                                                                   | Beschreibung                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -oder [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor | Wenn die WinSNMP-Anwendung den Arbeitsspeicher zuordnet, muss Sie den Speicher mit einem aufzurufenden Befehl für eine entsprechende Funktion nicht mehr zuordnen. Wenn die-Implementierung den Arbeitsspeicher zuordnet, muss die Anwendung die [**snmpfredescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufzurufen, um den Arbeitsspeicher freizugeben. |
| [**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) -Struktur                                    | Wenn der **Wertmember** ein [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -oder [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor ist, muss die Anwendung wie oben beschrieben für Deskriptoren fortgesetzt werden.                                                                                                     |
| Ressourcen handle                                                               | Die-Implementierung ordnet den Speicher zu, verwaltet ihn und gibt ihn frei.                                                                                                                                                                                                                         |
| Zeichenfolge im C-Stil                                                                | Die Anwendung WinSNMP muss den zugewiesenen Speicher verwalten und freigeben.                                                                                                                                                                                                                |



 

Weitere Informationen finden Sie unter [Freigeben von WinSNMP-Deskriptoren](freeing-winsnmp-descriptors.md).

 

 





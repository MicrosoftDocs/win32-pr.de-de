---
title: Zuordnen von WinSNMP-Speicherobjekten
description: Deskriptoren, Ressourcenhandles und Zeichenfolgen im C-Stil sind die drei Typen von Speicherobjekten in der WinSNMP-Programmierumgebung.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1188af74e150313cb24b01886d06df9e3ad065039cad9fa4a3e0b3b5ee6a9f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009788"
---
# <a name="allocating-winsnmp-memory-objects"></a>Zuordnen von WinSNMP-Speicherobjekten

Deskriptoren, Ressourcenhandles und Zeichenfolgen im C-Stil sind die drei Typen von Speicherobjekten in der WinSNMP-Programmierumgebung.

Der Objekttyp bestimmt, ob die Microsoft WinSNMP-Implementierung oder die WinSNMP-Anwendung den Speicher für das Objekt zuteilen und seine Zuordnung wieder aufgibt. Dies reduziert die unnötige Zuordnung von temporärem Pufferspeicher und unnötiges Kopieren von Puffern.

In der folgenden Tabelle werden die Zuordnung und Freigabe von Ressourcen für WinSNMP-Speicherobjekte zusammengefasst.



| Objekttyp                                                                   | Beschreibung                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**smiOID-**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) [**oder smiOCTETS-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Wenn die WinSNMP-Anwendung den Arbeitsspeicher zuteilen, muss sie die Zuordnung des Arbeitsspeichers mit einem Aufruf einer entsprechenden Funktion aufteilen. Wenn die Implementierung den Arbeitsspeicher zuordne, muss die Anwendung die [**SnmpFreeDescriptor-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) aufrufen, um die Zuordnung des Arbeitsspeichers frei zu machen. |
| [**smiVALUE-Struktur**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Wenn der **Wert member** ein [**smiOID- oder**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) [**smiOCTETS-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ist, muss die Anwendung wie oben für Deskriptoren angegeben fortgesetzt werden.                                                                                                     |
| Ressourcenhand handle                                                               | Die Implementierung reserviert, verwaltet und gibt den Arbeitsspeicher frei.                                                                                                                                                                                                                         |
| Zeichenfolge im C-Stil                                                                | Die WinSNMP-Anwendung muss den von ihr reservierten Arbeitsspeicher verwalten und frei geben.                                                                                                                                                                                                                |



 

Weitere Informationen finden Sie unter [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).

 

 





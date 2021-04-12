---
title: Verwalten von Objekt bezeichlern
description: Die WinSNMP-API bietet mehrere WinSNMP-Hilfsprogrammfunktionen, die die Bearbeitung von Objekt Bezeichners für WinSNMP-Anwendungen vereinfachen.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471644"
---
# <a name="managing-object-identifiers"></a>Verwalten von Objekt bezeichlern

Die WinSNMP-API bietet mehrere [WinSNMP-Hilfsprogrammfunktionen](winsnmp-functions.md) , die die Bearbeitung von Objekt Bezeichners für WinSNMP-Anwendungen vereinfachen.

Die [**snmpoidtostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) -Funktion konvertiert die interne binäre Darstellung eines Objekt Bezeichners in das gepunktete numerische Zeichen folgen Format. Wenn Sie [**snmpoidtostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)aufzurufen, geben Sie einen Zeichen folgen Puffer mit der Länge maxobjidgersize (1408 Bytes) an, um sicherzustellen, dass der Ausgabepuffer groß genug für die konvertierte Zeichenfolge ist. Um einen Objekt Bezeichner aus dem Format der punktierten numerischen Zeichenfolge in seine interne binäre Darstellung zu konvertieren, müssen Sie die Funktion [**snmpstrautooid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) abrufen.

Zum Kopieren eines SNMP-Objekt Bezeichners wird die [**snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) -Funktion aufgerufen. Diese Funktion ordnet den erforderlichen Speicherplatz für den neuen Objekt Bezeichner zu.

Eine WinSNMP-Anwendung muss die [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufruft, um Ressourcen freizugeben, die für den **ptr** -Member der [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur reserviert sind, die sowohl durch die [**snmpstrautooid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) -als auch die [**snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) -Funktion angegeben wird

Die [**snmpoidcompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) -Funktion vergleicht zwei SNMP-Objekt Bezeichner. Die WinSNMP-Anwendung kann die Anzahl der zu vergleichenden untergeordneten Elemente angeben. Rufen Sie **snmpoidcompare** auf, um zu bestimmen, ob zwei Objekt Bezeichner über allgemeine Präfixe verfügen.

Weitere Informationen zum Verwalten des Arbeitsspeichers, der den Objekt Bezeichners zugeordnet ist, finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).

 

 





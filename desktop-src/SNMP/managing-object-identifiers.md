---
title: Verwalten von Objektbezeichnern
description: Die WinSNMP-API bietet mehrere WinSNMP-Hilfsfunktionen, die die Bearbeitung von Objektbezeichnern für WinSNMP-Anwendungen vereinfachen.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362adbf445901f25307452d67c313ef2a8d0ac5aea038ebfcf61863a72370cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009418"
---
# <a name="managing-object-identifiers"></a>Verwalten von Objektbezeichnern

Die WinSNMP-API bietet mehrere [WinSNMP-Hilfsfunktionen,](winsnmp-functions.md) die die Bearbeitung von Objektbezeichnern für WinSNMP-Anwendungen vereinfachen.

Die [**SnmpOidToStr-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) konvertiert die interne binäre Darstellung eines Objektbezeichners in das gepunktete numerische Zeichenfolgenformat. Wenn Sie [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)aufrufen, geben Sie einen Zeichenfolgenpuffer der Länge MAXOBJIDSTRSIZE (1408 Bytes) an, um sicherzustellen, dass der Ausgabepuffer groß genug ist, um die konvertierte Zeichenfolge zu speichern. Um einen Objektbezeichner aus dem gepunkteten numerischen Zeichenfolgenformat in seine interne binäre Darstellung zu konvertieren, rufen Sie die [**SnmpStrToOid-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) auf.

Um einen SNMP-Objektbezeichner zu kopieren, rufen Sie die [**SnmpOidCopy-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) auf. Diese Funktion ordnet den erforderlichen Arbeitsspeicher für den neuen Objektbezeichner zu.

Eine WinSNMP-Anwendung muss die [**SnmpFreeDescriptor-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) aufrufen, um Ressourcen frei zu machen, die dem **ptr-Member** der [**smiOID-Struktur**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) zugeordnet sind, die sowohl von den [**Funktionen SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) als [**auch SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) angegeben wird.

Die [**SnmpOidCompare-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) vergleicht zwei SNMP-Objektbezeichner. Die WinSNMP-Anwendung kann die Anzahl der zu vergleichenden Unteridentitäten angeben. Rufen Sie **SnmpOidCompare** auf, um zu bestimmen, ob zwei Objektbezeichner gemeinsame Präfixe aufweisen.

Weitere Informationen zum Verwalten des Speichers, der für Objektbezeichner zugeordnet ist, finden Sie unter [Zuordnen von WinSNMP-Speicherobjekten.](allocating-winsnmp-memory-objects.md)

 

 





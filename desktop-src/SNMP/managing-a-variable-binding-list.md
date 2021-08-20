---
title: Verwalten einer Variablenbindungsliste
description: Die SnmpGetVb-Funktion ruft Variablenbindungsinformationen aus einer Variablenbindungsliste ab. Die Funktion ruft den Variablennamen und den zugeordneten Wert der Variablen aus dem Variablenbindungseintrag ab, der von der WinSNMP-Anwendung angegeben wird.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c382e2780ae49a1f029aab2cfef2bcd4357fcfbf7b37ce9a1fcad9aed5bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009448"
---
# <a name="managing-a-variable-binding-list"></a>Verwalten einer Variablenbindungsliste

Die [**SnmpGetVb-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) ruft Variablenbindungsinformationen aus einer Variablenbindungsliste ab. Die Funktion ruft den Variablennamen und den zugeordneten Wert der Variablen aus dem Variablenbindungseintrag ab, der von der WinSNMP-Anwendung angegeben wird.

Um Variablenbindungseinträge in einer Variablenbindungsliste zu aktualisieren, rufen Sie die [**SnmpSetVb-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) auf. Die **SnmpSetVb-Funktion** fügt auch neue Variablenbindungseinträge an eine vorhandene Variablenbindungsliste an.

Die WinSNMP-Anwendung muss die [**SnmpDeleteVb-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) aufrufen, um Einträge aus einer Variablenbindungsliste zu entfernen.

Zum Abrufen, Ändern oder Löschen eines Variablenbindungseintrags muss die WinSNMP-Anwendung die Position des Eintrags in der Variablenbindungsliste angeben.

Ein Aufruf der [**SnmpSetPduData-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) ordnet eine Variablenbindungsliste einer PDU zu. Ein Aufruf der [**SnmpGetPduData-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) ruft eine Variablenbindungsliste von einem PDU ab. Eine einzelne Variablenbindung ist nicht direkt einer PDU zugeordnet, sondern indirekt durch die Aufnahme in eine Variablenbindungsliste.

 

 





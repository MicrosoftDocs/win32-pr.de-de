---
title: Öffnen und Schließen einer WinSNMP-Sitzung
description: Um eine Sitzung zu öffnen, ruft eine Anwendung die SnmpCreateSession-Funktion auf.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41871c9adc2f7fcefc04b5816b29685ad6b1516a6238c1855ed41e878d5b2736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009198"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Öffnen und Schließen einer WinSNMP-Sitzung

Um eine Sitzung zu öffnen, ruft eine Anwendung die [**SnmpCreateSession-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) auf. Wenn die Funktion erfolgreich abgeschlossen wurde, öffnet die Microsoft WinSNMP-Implementierung eine Sitzung, und die Funktion gibt einen Sitzungsbezeichner in Form eines **HSNMP \_ SESSION-Handles** zurück. Alle WinSNMP-Funktionen, die Handlevariablen zurückgeben, enthalten den Sitzungsbezeichner als Eingabeparameter. Dadurch kann die Implementierung das Handle verwenden, um Ressourcen effizient auf Sitzungsebene zu verwalten.

Für eine Anwendung können mehrere Sitzungen gleichzeitig geöffnet sein. Mehrere Sitzungen innerhalb einer Anwendung können Handlevariablen gemeinsam nutzen.

Wenn die Implementierung aufgrund von Ressourceneinschränkungen keine Sitzung öffnen kann, wird SNMPAPI \_ FAILURE zurückgegeben, wenn die Anwendung [**SnmpCreateSession aufruft.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) Wenn die Anwendung dann die [**SnmpGetLastError-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) aufruft, wird SNMPAPI \_ ALLOC \_ ERROR zurückgegeben.

Durch einen Aufruf der [**SnmpClose-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) kann die Implementierung alle verbleibenden Ressourcen freigeben und die Sitzung schließen.

Weitere Informationen finden Sie unter [Ressourcenhandleobjekte](resource-handle-objects.md) und [WinSNMP-Sitzungen.](winsnmp-sessions.md)

 

 





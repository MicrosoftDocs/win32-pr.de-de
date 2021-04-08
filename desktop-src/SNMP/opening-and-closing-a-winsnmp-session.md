---
title: Öffnen und Schließen einer WinSNMP-Sitzung
description: Um eine Sitzung zu öffnen, ruft eine Anwendung die snmpkreatesession-Funktion auf.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037286"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Öffnen und Schließen einer WinSNMP-Sitzung

Um eine Sitzung zu öffnen, ruft eine Anwendung die [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) -Funktion auf. Wenn die Funktion erfolgreich abgeschlossen wird, wird von der Microsoft WinSNMP-Implementierung eine Sitzung geöffnet, und die Funktion gibt einen Sitzungs Bezeichner in Form eines **hsnmp- \_ Sitzungs** Handles zurück. Alle WinSNMP-Funktionen, die Handle-Variablen zurückgeben, enthalten den Sitzungs Bezeichner als Eingabeparameter. Dadurch kann die Implementierung das Handle verwenden, um Ressourcen auf Sitzungs Ebene effizient zu verwalten.

In einer Anwendung können mehrere Sitzungen gleichzeitig geöffnet sein. Mehrere Sitzungen in einer Anwendung können Handle-Variablen freigeben.

Wenn die Implementierung eine Sitzung aufgrund von Ressourceneinschränkungen nicht öffnen kann, wird ein Snmpapi-Fehler zurückgegeben, \_ Wenn die Anwendung [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)aufruft. Wenn die Anwendung dann die [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) -Funktion aufruft, gibt Sie den Fehler "Snmpapi-Zuweisung" zurück \_ \_ .

Ein Aufrufe der [**snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) -Funktion ermöglicht der Implementierung, alle verbleibenden Ressourcen freizugeben und die Sitzung zu schließen.

Weitere Informationen finden Sie unter [resource handle-Objekte](resource-handle-objects.md) und [WinSNMP-Sitzungen](winsnmp-sessions.md).

 

 





---
title: Ressourcenhandle-Objekte
description: Die Struktur eines Ressourcen Objekts ist auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann mit einem Handle auf ein Ressourcen Objekt zugreifen.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713061"
---
# <a name="resource-handle-objects"></a>Ressourcenhandle-Objekte

Die Struktur eines Ressourcen Objekts ist auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann mit einem Handle auf ein Ressourcen Objekt zugreifen.

Die-Implementierung kann einen der folgenden Typen von Ressourcen Handles für eine WinSNMP-Anwendung zuordnen.

| Handle-Typ        | BESCHREIBUNG                       |
|--------------------|-----------------------------------|
| **hsnmp- \_ Sitzung** | Handle für eine WinSNMP-Sitzung       |
| **hsnmp- \_ Entität**  | Handle für eine SNMP-Entität          |
| **hsnmp- \_ Kontext** | Handle für einen WinSNMP-Kontext       |
| **hsnmp- \_ PDU**     | Handle für eine Protokolldaten Einheit    |
| **hsnmp- \_ VBL**     | Handle für eine Variablen Bindungs Liste |



 

Eine WinSNMP-Anwendung kann anfordern, dass die Implementierung Ressourcen Handles erstellt oder löscht, aber die Implementierung führt den Vorgang aus. Weitere Informationen zum Freigeben einzelner Ressourcen finden Sie in den Funktionen " [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)", " [**snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)", " [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)", " [**snmpfreeentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)" und " [**snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) ".

 

 





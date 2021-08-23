---
title: Resource Handle-Objekte
description: Die Struktur eines Ressourcenobjekts ist auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann mit einem Handle auf ein Ressourcenobjekt zugreifen.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b05702f0ad43e5b4b80a9b1a3cada471212dec3bc377bddcc95fe9a109ec78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009118"
---
# <a name="resource-handle-objects"></a>Resource Handle-Objekte

Die Struktur eines Ressourcenobjekts ist auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann mit einem Handle auf ein Ressourcenobjekt zugreifen.

Die Implementierung kann einen der folgenden Arten von Ressourcenhandles für eine WinSNMP-Anwendung zuordnen.

| Handletyp        | BESCHREIBUNG                       |
|--------------------|-----------------------------------|
| **HSNMP-SITZUNG \_** | Behandeln einer WinSNMP-Sitzung       |
| **HSNMP-ENTITÄT \_**  | Handle für eine SNMP-Entität          |
| **HSNMP-KONTEXT \_** | Handle für einen WinSNMP-Kontext       |
| **HSNMP \_ PDU**     | Handle für eine Protokolldateneinheit    |
| **HSNMP \_ VBL**     | Handle für eine Variablenbindungsliste |



 

Eine WinSNMP-Anwendung kann anfordern, dass die Implementierung Ressourcenhandles erstellt oder löscht, aber die Implementierung führt den Vorgang aus. Weitere Informationen zum Freigegeben einzelner Ressourcen finden Sie in den Funktionen [**SnmpFreeDescriptor,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) [**SnmpFreeVbl,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) [**SnmpFreePdu,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)und [**SnmpFreeContext.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)

 

 





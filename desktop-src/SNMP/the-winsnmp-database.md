---
title: Die WinSNMP-Datenbank
description: Die Microsoft WinSNMP-Implementierung verwaltet einen Speicher mit Administratorinformationen in einer Datenbank.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f478c9bb1c05d3a094e2a15fac0a9cef5968f245257a0702d045eb90bd2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886000"
---
# <a name="the-winsnmp-database"></a>Die WinSNMP-Datenbank

Die Microsoft WinSNMP-Implementierung verwaltet einen Speicher mit Administratorinformationen in einer Datenbank. Die Datenbank enthält die folgenden Informationen:

-   Netzwerk- und Versionseigenschaften.

    Die Implementierung verwendet diese Eigenschaften, um zu bestimmen, welches Netzwerktransportprotokoll und welches SNMP-Versionsframework zum Abschließen von Übertragungsanforderungen verwendet werden sollen. Weitere Informationen finden Sie unter [Informationen zu SNMP-Versionen.](about-snmp-versions.md)

-   Entitäts- und Kontextübersetzungsmodus.

    Die Implementierung verwendet diesen Modus, um benutzerfreundliche Namen für SNMP-Entitäten und -Kontexte zu interpretieren. Weitere Informationen finden Sie unter [Festlegen des Entitäts- und Kontextübersetzungsmodus.](setting-the-entity-and-context-translation-mode.md)

-   Richtlinieneinstellung für erneute Übertragung.

    Die Implementierung verwendet diese Einstellung, um zu bestimmen, ob die Neuübertragungsrichtlinie der Anwendung ausgeführt werden soll. Die Implementierung speichert einen Time out-Wert und eine Wiederholungsanzahl für jede Zielentität. Weitere Informationen finden Sie unter [Informationen zur Neuübertragung](about-retransmission.md) und [Verwalten der Neuübertragungsrichtlinie.](managing-the-retransmission-policy.md)

 

 





---
title: Öffnen und Schließen einer WinSNMP-Anwendung
description: Die WinSNMP-Anwendung muss die SnmpStartup-Funktion erfolgreich aufrufen, bevor Sie eine andere WinSNMP-Funktion aufruft.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037288"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Öffnen und Schließen einer WinSNMP-Anwendung

Die WinSNMP-Anwendung muss die [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion erfolgreich aufrufen, bevor Sie eine andere WinSNMP-Funktion aufruft. Die **SnmpStartup** -Funktion ermöglicht es der Microsoft WinSNMP-Implementierung, Initialisierungs Prozeduren auszuführen. Die Funktion kehrt auch zur Anwendung der Version der WinSNMP-API zurück, die von der Implementierung unterstützt wird, der Ebene der unterstützten SNMP-Kommunikation und der standardmäßigen Übersetzungs-und Neuübertragungs Modi der Implementierung.

Die Anwendung WinSNMP muss die Funktion [**snmpcleanup aufgerufen werden**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) , wenn die Anwendung die Dienste der Implementierung nicht mehr benötigt. Obwohl **snmpcleanup** es der Implementierung ermöglicht, alle der Anwendung zugeordneten Ressourcen freizugeben, wird empfohlen, dass die Anwendung zuerst die [**snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) -Funktion für jede geöffnete WinSNMP-Sitzung aufruft, um die Leistung der Implementierung zu maximieren. Die WinSNMP-Anwendung muss [**snmpcleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) als letzte WinSNMP-Funktion ausführen, bevor Sie beendet wird.

 

 





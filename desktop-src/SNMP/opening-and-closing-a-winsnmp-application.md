---
title: Öffnen und Schließen einer WinSNMP-Anwendung
description: Die WinSNMP-Anwendung muss die SnmpStartup-Funktion erfolgreich aufrufen, bevor sie eine andere WinSNMP-Funktion aufruft.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aa18f437f8b1a430ad27b40b838859d2e00641bcb4532602715548b370acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009248"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Öffnen und Schließen einer WinSNMP-Anwendung

Die WinSNMP-Anwendung muss die [**SnmpStartup-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) erfolgreich aufrufen, bevor sie eine andere WinSNMP-Funktion aufruft. Die **SnmpStartup-Funktion** ermöglicht der Microsoft WinSNMP-Implementierung das Ausführen von Initialisierungsverfahren. Die Funktion gibt auch die Version der WinSNMP-API, die von der Implementierung unterstützt wird, die Ebene der unterstützten SNMP-Kommunikation und die Standardübersetzungs- und Neuübertragungsmodi der Implementierung an die Anwendung zurück.

Die WinSNMP-Anwendung muss die [**SnmpCleanup-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) aufrufen, wenn die Anwendung die Dienste der Implementierung nicht mehr benötigt. Obwohl **SnmpCleanup** es der Implementierung ermöglicht, alle ressourcen, die der Anwendung zugeordnet sind, freizugeben, wird empfohlen, dass die Anwendung zuerst einmal die [**SnmpClose-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) für jede geöffnete WinSNMP-Sitzung aufruft, um die Leistung der Implementierung zu maximieren. Die WinSNMP-Anwendung muss [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) als letzte WinSNMP-Funktion aufrufen, bevor sie beendet wird.

 

 





---
title: Schreiben von WinSNMP-Anwendungen mit mehreren Threads
description: Die Microsoft WinSNMP-Implementierung stellt sicher, dass die WinSNMP-Vorgänge eines Prozesses die WinSNMP-Einstellungen eines anderen Prozesses nicht ändern.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ee400009204a1117eb54b8166ade2c10f3d1dd3317a8316d70fc8c2d606d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142733"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Schreiben von WinSNMP-Anwendungen mit mehreren Threads

Die Microsoft WinSNMP-Implementierung stellt sicher, dass die WinSNMP-Vorgänge eines Prozesses die WinSNMP-Einstellungen eines anderen Prozesses nicht ändern.

Eine WinSNMP-Anwendung mit mehreren Threads muss sicherstellen, dass WinSNMP-Vorgänge, die Parameter auf Anwendungsebene festlegen, threadsicher sind. Die Funktionen, die Parameter auf Anwendungsebene festlegen, sind [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) und [**SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) Diese Funktionen ändern die Einstellungen für den Entitäts- und Kontextübersetzungsmodus und den Neuübertragungsmodus.

Weitere Informationen finden Sie unter [Mehrere Threads](/windows/desktop/ProcThread/multiple-threads) und [Threadsicherheit und Zugriffsrechte.](/windows/desktop/ProcThread/thread-security-and-access-rights)

 

 
---
title: Konfigurieren von RPC für SPX/IPX
description: Bei Verwendung der ipx-Transporte ncacn spx und ncadg ist der Servername identisch mit dem Servernamen \_ \_ auf Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5557541b296c436f2c3c1de007eb0e331e1c77d0529be83e758a25b76ac5e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022450"
---
# <a name="configuring-rpc-for-spxipx"></a>Konfigurieren von RPC für SPX/IPX

Bei Verwendung der **\_ ipx-Transporte ncacn spx** und **ncadg \_** ist der Servername identisch mit dem Servernamen auf Windows. Da die Namen jedoch mithilfe von Protokollen von Werden verteilt werden, müssen sie den Benennungskonventionen von Bein entsprechen. Wenn es sich bei einem Servernamen nicht um einen gültigen Namen handelt, können Server keine Endpunkte mit den **ncacn \_ spx-** oder **ncadg-IPX-Transporten \_** erstellen.

Ein gültiger Name des Servers Von Einer enthält nur die Zeichen zwischen 0x20 und 0x7f. Kleinbuchstaben werden in Großbuchstaben geändert. Die folgenden Zeichen können nicht verwendet werden:

" \* ,./:;<=>?\[\]\\\|\]

Um die Kompatibilität mit der ersten Version von Windows NT zu gewährleisten, können Sie mit **ncacn \_ spx** und **ncadg \_ ipx** auch ein spezielles Format des Servernamens verwenden, das als Tildename bezeichnet wird. Der Tildename besteht aus einer Tilde (~), gefolgt von der achtstelligen Netzwerknummer des Servers und anschließend der 12-stelligen Ethernet-Adresse. Tildenamen haben einen Vorteil, da sie keine Namensdienstfunktionen erfordern. Wenn Sie also mit einem Server verbunden sind, funktioniert der Tildename.

Die folgenden Tabellen enthalten zwei Beispielkonfigurationen, die die zuvor beschriebenen Punkte veranschaulichen.



| Komponente                            | Konfiguriert als      |
|--------------------------------------|--------------------|
| Windows-Server                       | NWCS               |
| Windows-Client                       | NWCS               |
| 16-Bit-Windows, MS-DOS-Client | NetWare-Redirector |



 

Die Konfiguration in der vorherigen Tabelle erfordert, dass Sie über NetWare-Dateiserver oder -Router in Ihrem Netzwerk verfügen. Dadurch wird die beste Leistung erzeugt, da die Servernamen in der NetWare Bindery gespeichert werden.



| Komponente                            | Konfiguriert als |
|--------------------------------------|---------------|
| Windows-Server                       | SAP-Agent     |
| Windows-Client                       | IPX/SPX       |
| 16-Bit-Windows, MS-DOS-Client | IPX/SPX       |



 

Die zweite Konfiguration funktioniert in einer Umgebung, die keine NetWare-Dateiserver oder -Router enthält (z. B. ein Netzwerk von zwei Computern: ein Windows-Server und ein MS-DOS-Client). Die Namensauflösung, die beim ersten Aufruf über ein Bindungshand handle erfolgt, ist etwas langsamer als in der ersten Konfiguration. Darüber hinaus führt die zweite Konfiguration zu mehr Datenverkehr, der über das Netzwerk generiert wird.

Wenn ein RPC-Server einen SPX- oder IPX-Endpunkt verwendet, werden der Servername und der Endpunkt als SAP-Server (Service Advertising Protocol) vom Typ 640 (hexadezimal) registriert, um die Namensauflösung zu implementieren. Um einen Servernamen aufzulösen, sendet der RPC-Client eine SAP-Anforderung für alle Dienste desselben Typs und scannt dann die Liste der Antworten nach dem Namen des Servers. Dieser Prozess erfolgt während des ersten RPC-Aufrufs über jedes Bindungshand handle. Weitere Informationen zum SAP-Protokoll fürEs finden Sie in ihrer NetWare-Dokumentation.

> [!Note]  
> Die 16-Bit-Windows-Clientanwendungen, die die ipx-Transporte **ncacn \_ spx** oder **ncadg \_** verwenden, erfordern, dass die Datei Nwipxspx.dll installiert wird, um unter dem WOW-Subsystem ausgeführt zu werden. Wenden Sie sich an Den, um diese Datei zu erhalten.

 

 

 





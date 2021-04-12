---
title: Konfigurieren von RPC für SPX/IPX
description: Bei Verwendung der ncacn \_ -SPX-und ncadg- \_ IPX-Transporte ist der Servername genau mit dem Servernamen unter Windows identisch.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471508"
---
# <a name="configuring-rpc-for-spxipx"></a>Konfigurieren von RPC für SPX/IPX

Bei Verwendung der **ncacn- \_ SPX** -und **ncadg- \_ IPX** -Transporte ist der Servername genau mit dem Servernamen unter Windows identisch. Da die Namen jedoch mithilfe von Novell-Protokollen verteilt werden, müssen Sie den Novell-Benennungs Konventionen entsprechen. Wenn es sich bei einem Servernamen nicht um einen gültigen Novell-Namen handelt, können Server mit den **ncacn- \_ SPX** -oder **ncadg- \_ IPX** -Transporten keine Endpunkte erstellen.

Ein gültiger Novell-Servername enthält nur die Zeichen zwischen 0x20 und 0x7F. Kleinbuchstaben werden in Großbuchstaben geändert. Die folgenden Zeichen können nicht verwendet werden:

" \* ,./:; <=>?\[\]\\\|\]

Um die Kompatibilität mit der ersten Version von Windows NT zu gewährleisten, können Sie mit **ncacn \_ SPX** und **ncadg \_ IPX** auch ein spezielles Format des Server namens verwenden, der als Tilde-Name bezeichnet wird. Der Tilde-Name besteht aus einer Tilde (~), gefolgt von der achtstelligen Netzwerk Nummer des Servers und gefolgt von der 12-stelligen Ethernet-Adresse. Tilde-Namen haben einen Vorteil, dass keine Namensdienst Funktionen erforderlich sind. Wenn Sie also mit einem Server verbunden sind, funktioniert der Tilde-Name.

Die folgenden Tabellen enthalten zwei Beispielkonfigurationen, die die zuvor beschriebenen Punkte veranschaulichen.



| Komponente                            | Konfiguriert als      |
|--------------------------------------|--------------------|
| Windows-Server                       | NWCS               |
| Windows-Client                       | NWCS               |
| 16-Bit-Windows-Client, MS-DOS-Client | NetWare-Redirector |



 

Für die Konfiguration in der vorherigen Tabelle ist es erforderlich, dass Sie über NetWare-Dateiserver oder Router im Netzwerk verfügen. Dies führt zu einer optimalen Leistung, da die Servernamen in der NetWare Bindery gespeichert werden.



| Komponente                            | Konfiguriert als |
|--------------------------------------|---------------|
| Windows-Server                       | SAP-Agent     |
| Windows-Client                       | IPX/SPX       |
| 16-Bit-Windows-Client, MS-DOS-Client | IPX/SPX       |



 

Die zweite Konfiguration funktioniert in einer Umgebung, die keine NetWare-Dateiserver oder-Router enthält (z. b. ein Netzwerk mit zwei Computern: ein Windows-Server und ein MS-DOS-Client). Die Namensauflösung, die während des ersten Aufrufens eines Bindungs Handles erreicht wird, ist etwas langsamer als bei der ersten Konfiguration. Außerdem führt die zweite Konfiguration zu mehr Datenverkehr, der über das Netzwerk generiert wird.

Wenn ein RPC-Server einen SPX-oder IPX-Endpunkt verwendet, werden der Servername und der Endpunkt als Dienst Ankündigungs Protokoll (SAP-Server) vom Typ 640 (hexadezimal) registriert, um die Namensauflösung zu implementieren. Zum Auflösen eines Server namens sendet der RPC-Client eine SAP-Anforderung für alle Dienste desselben Typs und scannt dann die Liste der Antworten auf den Namen des Servers. Dieser Prozess tritt während des ersten RPC-Aufrufs über die einzelnen Bindungs Handles auf. Weitere Informationen zum SAP-Protokoll für Novell finden Sie in der NetWare-Dokumentation.

> [!Note]  
> Die 16-Bit-Windows-Client Anwendungen, die die **ncacn- \_ SPX** -oder **ncadg- \_ IPX** -Transporte verwenden, erfordern, dass die Datei installiert Nwipxspx.dll, um unter dem wow-Subsystem ausgeführt werden zu können. Wenden Sie sich an Novell, um diese Datei zu erhalten.

 

 

 





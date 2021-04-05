---
title: RAS-Server und-Port Verwaltung
description: Mit den RAS-Server-Verwaltungsfunktionen können Sie Informationen zu einem angegebenen RAS-Server und seinen Ports erhalten. Mit diesen Funktionen können Sie auch eine Verbindung auf einem angegebenen RAS-Serverport beenden.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af21dfeda38a1c1147bf864a1fa1959092ac946
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037235"
---
# <a name="ras-server-and-port-administration"></a>RAS-Server und-Port Verwaltung

Mit den RAS-Server-Verwaltungsfunktionen können Sie Informationen zu einem angegebenen RAS-Server und seinen Ports erhalten. Mit diesen Funktionen können Sie auch eine Verbindung auf einem angegebenen RAS-Serverport beenden.

Die [**rasadminservergetinfo**](rasadminservergetinfo.md) -Funktion gibt eine [**RAS-Server- \_ \_ 0**](ras-server-0-str.md) -Struktur zurück, die Informationen zur Konfiguration eines RAS-Servers enthält. Die zurückgegebenen Informationen enthalten die Anzahl der Ports, die derzeit für die Verbindung verfügbar sind, die Anzahl der derzeit verwendeten Ports und die Server Versionsnummer.

Die [**rasadminportenum**](rasadminportenum.md) -Funktion Ruft ein Array von [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Strukturen ab, das Informationen für jeden der auf einem RAS-Server konfigurierten Ports enthält. Die Informationen zu den einzelnen Ports umfassen Folgendes:

-   Der Name des Ports
-   Informationen zu dem Gerät, das mit dem Port verbunden ist
-   Gibt an, ob der dem Port zugeordnete RAS-Server ein Windows NT/Windows 2000-Server ist.
-   Gibt an, ob der Port zurzeit verwendet wird und ob es sich um Informationen zur Verbindung handelt.

Sie können die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion aufrufen, um zusätzliche Informationen über einen angegebenen Port auf einem RAS-Server zu erhalten. Diese Funktion gibt eine Struktur des [**RAS- \_ Ports \_ 1**](ras-port-1-str.md) zurück, die eine [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) -Struktur und zusätzliche Informationen über den aktuellen Status des Ports enthält. Die **rasadminportgetinfo** -Funktion gibt auch ein Array von [**RAS- \_ Parameter**](ras-parameters-str.md) Strukturen zurück, die die Werte von medienspezifischen Schlüsseln beschreiben, die dem Port zugeordnet sind. Eine **RAS- \_ Parameter** Struktur verwendet einen Wert aus der RAS-parametriams- [**\_ \_ formatenumeration**](ras-params-format-str.md) , um das Format des Werts für jeden medienspezifischen Schlüssel anzugeben.

Die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion gibt auch eine [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) Struktur zurück, die verschiedene Statistik Leistungsindikatoren für die aktuelle Verbindung (sofern vorhanden) auf dem Port enthält. Bei einem Port, der Teil einer Verbindung mit mehreren Links ist, gibt **rasadminportgetinfo** Statistiken für den einzelnen Port und die kumulierten Statistiken für alle an der Verbindung beteiligten Ports zurück. Mit der [**rasadminportclearstatistics**](rasadminportclearstatistics.md) -Funktion können Sie die Statistik Zähler für den Port zurücksetzen. Die [**rasadminportdisconnect**](rasadminportdisconnect.md) -Funktion trennt den verwendeten Port.

Verwenden Sie die [**rasadminfreebuffer**](rasadminfreebuffer.md) -Funktion, um Arbeitsspeicher freizugeben, der von den Funktionen [**rasadminportenum**](rasadminportenum.md) und [**rasadminportgetinfo**](rasadminportgetinfo.md) zugewiesen wird. Verwenden Sie die [**rasadmingeterrorstring**](rasadmingeterrorstring.md) -Funktion, um eine Zeichenfolge abzurufen, die einen RAS-Fehlercode beschreibt, der von einer der RAS-Server Verwaltungsfunktionen (rasadmin) zurückgegeben wurde.

 

 





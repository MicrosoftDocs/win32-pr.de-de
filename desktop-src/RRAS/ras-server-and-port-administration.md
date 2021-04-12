---
title: Informationen zur RAS-Server-und-Port Verwaltung
description: Die RAS-Server-Verwaltungsfunktionen erhalten Informationen zu einem angegebenen RAS-Server und den zugehörigen Ports. Diese Funktionen werden auch verwendet, um eine Verbindung auf einem angegebenen RAS-Serverport zu beenden.
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- RAS-Verwaltung-RRAS, Server-und Port Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104472068"
---
# <a name="about-ras-server-and-port-administration"></a>Informationen zur RAS-Server-und-Port Verwaltung

Die RAS-Server-Verwaltungsfunktionen erhalten Informationen zu einem angegebenen RAS-Server und den zugehörigen Ports. Diese Funktionen werden auch verwendet, um eine Verbindung auf einem angegebenen RAS-Serverport zu beenden.

Die [**mpradminservergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) -Funktion gibt eine [**MPR \_ Server \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0) -Struktur zurück, die Informationen zur Konfiguration eines RAS-Servers enthält. Die zurückgegebenen Informationen enthalten die Anzahl der Ports, die derzeit für Verbindungen verfügbar sind, die Anzahl der derzeit verwendeten Ports und die Server Versionsnummer.

Die [**mpradminportenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) -Funktion Ruft ein Array von [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) -Strukturen ab. Jede Struktur enthält Informationen zu einem der Ports, die auf einem RAS-Server konfiguriert sind. Die Informationen zu den einzelnen Ports umfassen Folgendes:

-   Der Name des Ports
-   Informationen zu dem Gerät, das mit dem Port verbunden ist
-   Gibt an, ob der dem Port zugeordnete RAS-Server ein Windows NT/Windows 2000-Server ist.
-   Gibt an, ob der Port zurzeit verwendet wird und ob es sich um Informationen zur Verbindung handelt.

Zum Abrufen der Ports, die von einer bestimmten Verbindung verwendet werden, übergeben Sie [**mpradminportenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) ein Handle für diese Verbindung im *hconnection* -Parameter. Verwenden Sie die [**mpradminconnectionenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) -Funktion, um ein Handle für eine Verbindung zu erhalten. Wenn Sie eine RAS-Verwaltungs- [dll](ras-administration-dll.md)implementiert haben, erhalten die [**mpradminaccept**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) -und [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) -Funktionen alternativ ein Handle für jede neue Verbindung zum Zeitpunkt der Verbindungs Herstellung.

Sie können die [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) -Funktion aufrufen, um zusätzliche Informationen über einen angegebenen Port auf einem RAS-Server zu erhalten. Diese Funktion gibt eine Struktur des [**RAS- \_ Ports \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) zurück, die eine [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) -Struktur und zusätzliche Informationen über den aktuellen Status des Ports enthält. Die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion gibt auch ein Array von [**RAS- \_ Parameter**](ras-parameters-str.md) Strukturen zurück, die die Werte von medienspezifischen Schlüsseln beschreiben, die dem Port zugeordnet sind. Eine **RAS- \_ Parameter** Struktur verwendet einen Wert aus der RAS-parametriams- [**\_ \_ formatenumeration**](ras-params-format-str.md) , um das Format des Werts für jeden medienspezifischen Schlüssel anzugeben.

Die [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) -Funktion gibt auch eine [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) Struktur zurück, die verschiedene Statistik Leistungsindikatoren für die aktuelle Verbindung (sofern vorhanden) auf dem Port enthält. Bei einem Port, der Teil einer Verbindung mit mehreren Links ist, gibt **mpradminportgetinfo** Statistiken für den einzelnen Port und kumulierte Statistiken für alle an der Verbindung beteiligten Ports zurück. Sie können die [**mpradminportclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) -Funktion verwenden, um die Statistik Zähler für den Port zurückzusetzen. Die [**mpradminportdisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) -Funktion trennt den verwendeten Port.

Verwenden Sie die [**mpradminbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) -Funktion, um Arbeitsspeicher freizugeben, der von den Funktionen [**mpradminportenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) und [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) zugewiesen wird. Verwenden Sie die [**mpradmingeterrorstring**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) -Funktion, um eine Zeichenfolge abzurufen, die einen RAS-Fehlercode beschreibt, der von einer der RAS-Server Verwaltungsfunktionen (rasadmin) zurückgegeben wurde.

 

 





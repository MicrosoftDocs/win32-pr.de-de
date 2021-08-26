---
title: RAS-Server- und Portverwaltung
description: Mithilfe der RAS-Serververwaltungsfunktionen können Sie Informationen zu einem angegebenen RAS-Server und dessen Ports abrufen. Mit diesen Funktionen können Sie auch eine Verbindung an einem angegebenen RAS-Serverport beenden.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d09d683bf0850b5f51a5d9c1ac1aa21b25f2968ddedbed2d383d28dad7785f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028800"
---
# <a name="ras-server-and-port-administration"></a>RAS-Server- und Portverwaltung

Mithilfe der RAS-Serververwaltungsfunktionen können Sie Informationen zu einem angegebenen RAS-Server und dessen Ports abrufen. Mit diesen Funktionen können Sie auch eine Verbindung an einem angegebenen RAS-Serverport beenden.

Die [**RasAdminServerGetInfo-Funktion**](rasadminservergetinfo.md) gibt eine [**RAS SERVER \_ \_ 0-Struktur**](ras-server-0-str.md) zurück, die Informationen zur Konfiguration eines RAS-Servers enthält. Die zurückgegebenen Informationen umfassen die Anzahl der derzeit für die Verbindung verfügbaren Ports, die Anzahl der derzeit verwendeten Ports und die Serverversionsnummer.

Die [**RasAdminPortEnum-Funktion**](rasadminportenum.md) ruft ein Array von [**RAS PORT \_ \_ 0-Strukturen**](ras-port-0-str.md) ab, das Informationen zu jedem der ports enthält, die auf einem RAS-Server konfiguriert sind. Die Informationen für jeden Port umfassen Folgendes:

-   Der Name des Ports
-   Informationen zum Gerät, das an den Port angeschlossen ist
-   Gibt an, ob der dem Port zugeordnete RAS-Server ein Windows NT/Windows 2000-Server ist.
-   Gibt an, ob der Port derzeit verwendet wird, und , falls ja, Informationen zur Verbindung.

Sie können die [**RasAdminPortGetInfo-Funktion**](rasadminportgetinfo.md) aufrufen, um zusätzliche Informationen zu einem angegebenen Port auf einem RAS-Server abzurufen. Diese Funktion gibt eine [**RAS \_ PORT \_ 1-Struktur**](ras-port-1-str.md) zurück, die eine [**RAS PORT \_ \_ 0-Struktur**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) und zusätzliche Informationen zum aktuellen Zustand des Ports enthält. Die **RasAdminPortGetInfo-Funktion** gibt auch ein Array von [**RAS \_ PARAMETERS-Strukturen**](ras-parameters-str.md) zurück, die die Werte aller medienspezifischen Schlüssel beschreiben, die dem Port zugeordnet sind. Eine **RAS \_ PARAMETERS-Struktur** verwendet einen Wert aus der [**RAS \_ PARAMS \_ FORMAT-Enumeration,**](ras-params-format-str.md) um das Format des Werts für jeden medienspezifischen Schlüssel anzugeben.

Die [**RasAdminPortGetInfo-Funktion**](rasadminportgetinfo.md) gibt auch eine [**RAS PORT \_ \_ STATISTICS-Struktur**](ras-port-statistics-str.md) zurück, die verschiedene Statistikindikatoren für die aktuelle Verbindung am Port enthält, sofern vorhanden. Für einen Port, der Teil einer Multilinkverbindung ist, gibt **RasAdminPortGetInfo** Statistiken für den einzelnen Port und kumulative Statistiken für alle ports zurück, die an der Verbindung beteiligt sind. Sie können die [**RasAdminPortClearStatistics-Funktion**](rasadminportclearstatistics.md) verwenden, um die Statistikindikatoren für den Port zurückzusetzen. Die [**RasAdminPortDisconnect-Funktion**](rasadminportdisconnect.md) trennt einen verwendeten Port.

Verwenden Sie die [**RasAdminFreeBuffer-Funktion,**](rasadminfreebuffer.md) um den von den [**Funktionen RasAdminPortEnum**](rasadminportenum.md) und [**RasAdminPortGetInfo**](rasadminportgetinfo.md) belegten Arbeitsspeicher freizugeben. Verwenden Sie die [**RasAdminGetErrorString-Funktion,**](rasadmingeterrorstring.md) um eine Zeichenfolge abzurufen, die einen RAS-Fehlercode beschreibt, der von einer der RAS-Serververwaltungsfunktionen (RasAdmin) zurückgegeben wird.

 

 





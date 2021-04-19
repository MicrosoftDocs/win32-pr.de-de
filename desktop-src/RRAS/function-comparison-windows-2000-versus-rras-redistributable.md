---
title: Funktions Vergleich von Windows 2000 und RRAS Redistributable
description: Die RAS-API wird als Feature von Windows 2000 und neueren Betriebssystemen verteilt und ist als verteilbare Komponente für Windows NT 4,0 mit Service Pack 3 (SP3) und früher verfügbar.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341683"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>Funktions Vergleich: Windows 2000 und RRAS Redistributable

Die RAS-API wird als Feature von Windows 2000 und neueren Betriebssystemen verteilt und ist als verteilbare Komponente für Windows NT 4,0 mit Service Pack 3 (SP3) und früher verfügbar. RAS bietet die gleichen Funktionen in beiden Formularen, aber die verwendete Benennungs Konvention unterscheidet sich für die Verweis Elemente in jeder Version der RAS-API.

Die RAS-Funktionen für Windows NT 4,0 mit SP3 und früher beginnen in der Regel mit dem Präfix "rasadmin". Die analogen Funktionen für den Routing-und RAS-Dienst (RRAS) beginnen mit dem Präfix "mpradmin". Beispielsweise stellt RAS eine Funktion mit dem Namen [**rasadminportgetinfo**](rasadminportgetinfo.md)bereit. Die Analog-Funktion in RRAS heißt [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo). In einem ähnlichen Beispiel stellt RAS die Rückruffunktion [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md)bereit. RRAS bietet eine ähnliche Rückruffunktion mit dem Namen [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser). Ausnahmen für diese Regel sind [**rasadminportclearstatistics**](rasadminportclearstatistics.md), die unter RRAS den Wert [**mpradminportclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)und [**rasadminfreebuffer**](rasadminfreebuffer.md)hat, der unter RRAS den Wert [**mpradminbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)aufweist.

In der folgenden Tabelle werden die Windows NT 4,0 SP3-RAS-Funktionen und die zugehörigen RRAS-Funktionen aufgelistet.



| Windows NT 4,0-RAS                                                                   | RRAS                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Rasadminakzeptnewconnection**](rasadminacceptnewconnection.md)                   | [**Mpradminakzeptnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**Rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md) | [**Mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**Rasadminfrebuffer**](rasadminfreebuffer.md)                                     | [**Mpradminbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**Rasadmingeterrorstring**](rasadmingeterrorstring.md)                             | [**Mpradmingeterrorstring**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**Rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md)                   | [**Mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**Rasadminportclearstatistics**](rasadminportclearstatistics.md)                   | [**Mpradminportclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**Rasadminportdisconnect**](rasadminportdisconnect.md)                             | [**Mpradminportdisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**Rasadminportenum**](rasadminportenum.md)                                         | [**Mpradminportenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**Rasadminportgetinfo**](rasadminportgetinfo.md)                                   | [**Mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**Rasadminreleaseipaddress**](rasadminreleaseipaddress.md)                         | [**Mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**Rasadminusergetinfo**](rasadminusergetinfo.md)                                   | [**Mpradminusergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**Rasadminusereintinfo**](rasadminusersetinfo.md)                                   | [**Mpradminusereintinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

Obwohl die RRAS-Funktionen Windows NT 4,0 mit SP3 und früheren RAS-Entsprechungen in der Funktionalität ähneln, nehmen RRAS-Funktionen häufig einen anderen Satz von Parametern auf. Ausführliche Informationen zur Parameterliste der Funktion finden Sie auf der Referenzseite für eine bestimmte Funktion.

Die weitervertreibbare RRAS-Version für Windows NT 4,0 mit SP3 und früher fügt die folgenden Funktionen hinzu, die keine RAS-Entsprechungen aufweisen:

[**Mpradminakzeptnewlink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**Mpradminconnectionclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**Mpradminconnectionenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**Mpradminconnectiongetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**Mpradmingetpdcserver**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**Mpradminisservicerunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**Mpradminlinkhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**Mpradminportreset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**Mpradminserverconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**Mpradminserverdisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Zusätzlich zu den oben genannten Funktionen fügen die Betriebssysteme Windows 2000 und höher die folgenden Funktionen hinzu:

[**Mpradminsendusermessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 





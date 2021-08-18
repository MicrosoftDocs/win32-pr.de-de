---
title: Funktionsvergleich Windows 2000 im Vergleich zu RRAS Redistributable
description: Die RAS-API wird als Feature der Betriebssysteme Windows 2000 und höher verteilt und ist als verteilbare Version für Windows NT 4.0 mit Service Pack 3 (SP3) und früher verfügbar.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027c120133573b1d0c452b74dd02ab8fa0aa6f3367eb1a5fc9668a2de089c758
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995340"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>Funktionsvergleich: Windows 2000 im Vergleich zu RRAS Redistributable

Die RAS-API wird als Feature der Betriebssysteme Windows 2000 und höher verteilt und ist als verteilbare Version für Windows NT 4.0 mit Service Pack 3 (SP3) und früher verfügbar. RAS bietet die gleiche Funktionalität in beiden Formen, aber die verwendete Benennungskonvention ist für die Referenzelemente in jeder Version der RAS-API unterschiedlich.

Die RAS-Funktionen Windows NT 4.0 mit SP3 und früher beginnen in der Regel mit dem Präfix "RasAdmin". Die analogen Funktionen für routing and remote access service (RRAS) beginnen mit dem Präfix "MprAdmin". Ras stellt beispielsweise eine Funktion namens [**RasAdminPortGetInfo zurEnthalten.**](rasadminportgetinfo.md) Die analoge Funktion in RRAS heißt [**MprAdminPortGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) Als ähnliches Beispiel stellt RAS die Rückruffunktion [**RasAdminGetIpAddressForUser zurVerfingung von**](rasadmingetipaddressforuser.md). RRAS bietet eine ähnliche Rückruffunktion namens [**MprAdminGetIpAddressForUser.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) Ausnahmen von dieser Regel sind [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), das unter RRAS [**mprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)ist, und [**RasAdminFreeBuffer**](rasadminfreebuffer.md), was unter RRAS [**mprAdminBufferFree ist.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)

In der folgenden Tabelle sind die Windows NT 4.0 SP3 RAS-Funktionen und die entsprechenden RRAS-Funktionen aufgeführt.



| Windows NT 4.0 RAS                                                                   | Rras                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)                   | [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) | [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**RasAdminFreeBuffer**](rasadminfreebuffer.md)                                     | [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**RasAdminGetErrorString**](rasadmingeterrorstring.md)                             | [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)                   | [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)                   | [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**RasAdminPortDisconnect**](rasadminportdisconnect.md)                             | [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**RasAdminPortEnum**](rasadminportenum.md)                                         | [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**RasAdminPortGetInfo**](rasadminportgetinfo.md)                                   | [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)                         | [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**RasAdminUserGetInfo**](rasadminusergetinfo.md)                                   | [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**RasAdminUserSetInfo**](rasadminusersetinfo.md)                                   | [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

Obwohl die RRAS-Funktionen ihren Windows NT 4.0 mit SP3 und früheren RAS-Entsprechungen in der Funktionalität ähneln, verwenden RRAS-Funktionen häufig einen anderen Satz von Parametern. Vollständige Informationen zur Parameterliste dieser Funktion finden Sie auf der Referenzseite für eine bestimmte Funktion.

Das weiterverteilte RRAS für Windows NT 4.0 mit SP3 und früher fügt die folgenden Funktionen hinzu, die keine RAS-Entsprechungen haben:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Zusätzlich zu den obigen Funktionen fügen Windows Betriebssystemen 2000 und höher die folgenden Funktionen hinzu:

[**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 





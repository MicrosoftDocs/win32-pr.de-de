---
title: Null-Sitzungen
description: Manchmal kann ein in der NULL-Sitzung eintreffenden Rückruf wie ein authentifizierter-Rückruf erscheinen.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471660"
---
# <a name="null-sessions"></a>Null-Sitzungen

Manchmal kann ein in der NULL-Sitzung eintreffenden Rückruf wie ein authentifizierter-Rückruf erscheinen. Der Aufruf der [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) -Funktion gibt insbesondere die Authentifizierungs Ebene und den Sicherheitsanbieter zurück, die für den Aufruf verwendet werden. Dieser Vorgang bedeutet nicht, dass der-Befehl nicht für eine NULL-Sitzung verwendet wurde. Die beiden Probleme sind orthogonal. Bei Microsoft Windows 2000 kann ein Remote Prozedur Aufruf versuchen, die Identität eines Aufrufers anzunehmen und die Berechtigungen nach dem Identitätswechsel zu überprüfen. Unter Microsoft Windows XP ist es schneller, die [**rpcserverinqcallattribute**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) -Funktion aufzurufen und das **nullsession** -Flag zu überprüfen.

Ein weiterer relevanter Unterschied besteht zwischen Windows 2000 und Windows XP. Wenn nur das \_ Flag RPC if \_ Allow \_ Secure \_ only angegeben ist, werden Aufrufe in der NULL-Sitzung in Windows 2000 durchlaufen. In Windows XP werden bei der allgemeinen Verschärfung der Standard Sicherheitseinstellungen, wenn dieses Flag angegeben ist, Aufrufe der NULL-Sitzung mit "Zugriff verweigert" abgelehnt. Allerdings \_ \_ \_ \_ garantiert RPC nicht die Berechtigungsebene des aufrufenden Benutzers, auch wenn der RPC-Flag "Secure Secure only" verwendet wird. Alle RPC-Überprüfungen sind, dass der Benutzer über gültige Anmelde Informationen verfügt. Es ist möglich, dass der aufrufenden Benutzer das Gastkonto oder andere Konten mit niedrigen Berechtigungen verwendet. Stellen Sie sicher, dass der Server nicht über eine hohe Berechtigung verfügt, \_ Wenn RPC \_ \_ nur zulassen \_ verwendet wird.

 

 





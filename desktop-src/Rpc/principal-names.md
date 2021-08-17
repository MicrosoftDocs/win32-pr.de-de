---
title: Prinzipalnamen
description: Damit ein Client eine sich gegenseitig authentifizierte Sitzung mit einem Serverprogramm erstellen kann, muss er den erwarteten Prinzipalnamen des Servers angeben.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c0ba17916fb9f9c91ac959ea961c19d0f0a03e31d4caa11784dc123b54c5a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927219"
---
# <a name="principal-names"></a>Prinzipalnamen

Damit ein Client eine sich gegenseitig authentifizierte Sitzung mit einem Serverprogramm erstellen kann, muss er den erwarteten Prinzipalnamen des Servers angeben. Einige Protokolle, z. B. Kerberos, erfordern einen korrekten Serverprinzipalnamen für jede authentifizierte Sitzung. Ein Prinzipal ist eine Entität, die vom Sicherheitssystem erkannt wird. Dies schließt sowohl menschliche Benutzer als auch Systemdienste ein. Alle Prinzipalnamen haben ein ähnliches Format für einen bestimmten Sicherheitssupportanbieter (Security Support Provider, SSP). Ein SSP ist ein Softwaremodul, das die Sicherheitsüberprüfung durchführt. Weitere Informationen finden Sie unter [Übersicht über die SSPI-Architektur.](sspi-architectural-overview.md) Zur Aufrechterhaltung der Einheitlichkeit gibt ein Sicherheitsanbieter Systemdiensten in der Regel ähnliche Namen wie Benutzer. Bei einigen Sicherheitsanbietern haben Systemdienste möglicherweise keinen Prinzipalnamen.

Der Server registriert seinen Prinzipalnamen für den Sicherheitsanbieter mithilfe der [**RpcServerRegisterAuthInfo-Funktion.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) Für jeden Sicherheitsanbieter kann nur ein Serverprinzipalname verwendet werden. Wenn mehrere Namen registriert sind, wird nach dem Zufallsprinzip ein Name ausgewählt und verwendet. Der SSP bestimmt das Format des Prinzipalnamens. Beispielsweise sehen die Kerberos/Negotiate-SSPs für einen Systemdienst ungefähr wie folgt aus: \_ Computername$ @childdomain.parentdomain1.parentdomain2.COM .

Das empfohlene Verfahren zum Generieren von Prinzipalnamen ist die Verwendung dokumentierter APIs (z. B. die **DsMakeSpn-Funktion),** anstatt den Prinzipalnamen aus Zeichenfolgen zusammen zu setzen. Die Verwendung dokumentierter APIs erhöht die Portabilität zwischen verschiedenen Bereitstellungsumgebungen und beseitigt die Möglichkeit von Fehlern.

Die Angabe eines falschen Prinzipalnamens kann verhindern, dass client und server eine authentifizierte Sitzung einrichten. Der SCHANNEL-SSP verwendet Prinzipalnamen in einer von zwei Formen:

-   Das erste Formular für den SCHANNEL-Prinzipalnamen ist [*das msstd-Formular.*](m-glos.md) Namen in msstd-Form folgen in der Regel dem Muster msstd:servername@serverdomain.com . Dies wird als E-Mail-Namenseigenschaft bezeichnet. Wenn das Zertifikat eine E-Mail-Namenseigenschaft enthält und das at-Zeichen (@) enthält, ist der Prinzipalname msstd:email name. Andernfalls muss sie die Allgemeine Namenseigenschaft enthalten. Interne schräge Schrägstriche werden wie bei Zeichenfolgenbindungen verdoppelt.
-   Die zweite Form des SCHANNEL-Prinzipalnamens [*ist die vollständige*](f-glos.md) Form. Dies ist eine Reihe von RFC1779-kompatiblen Namen, die durch eckige Klammern und durch schräge Schrägstriche getrennt sind. Es folgt in der Regel dem Muster fullsic: \\ < \\ Authority \\ SubAuthority \\ ..... \\ Person> oder fullsic: \\ < \\ Authority \\ SubAuthority \\ ..... \\ ServerProgram->.

Wenn der Name nicht mit dem Zertifikat übereinstimmen sollte, wird ERROR \_ ACCESS \_ DENIED zurückgegeben. Wenn das Namensformat ungültig ist, gibt SCHANNEL SSP den Code ERROR \_ INVALID \_ PARAMETER zurück.

Zum Abfragen des Prinzipalnamens des Servers können Anwendungen [**RpcMgmtInqServerPrincName aufrufen.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) Dadurch wird eine auf NULL beendete Zeichenfolge zum Enthalten des Prinzipalnamens reserviert. Bevor sie beendet wird, muss Ihre Anwendung [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) aufrufen, um den Arbeitsspeicher freigibt, den diese Zeichenfolge belegt.

Das Abfragen des Servernamens auf diese Weise ist nicht sicher und sollte vermieden werden. Für die Serverauthentifizierung sollte das Clientprogramm wissen, mit welchem Server es eine Verbindung herstellen soll, und den Serverprinzipalnamen von Grund auf neu erstellen.

 

 





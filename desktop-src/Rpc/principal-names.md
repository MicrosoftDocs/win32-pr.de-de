---
title: Prinzipal Namen
description: Damit ein Client eine gegenseitig authentifizierte Sitzung mit einem Serverprogramm erstellen kann, muss er den erwarteten Prinzipal Namen des Servers bereitstellen.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471652"
---
# <a name="principal-names"></a>Prinzipal Namen

Damit ein Client eine gegenseitig authentifizierte Sitzung mit einem Serverprogramm erstellen kann, muss er den erwarteten Prinzipal Namen des Servers bereitstellen. Einige Protokolle, wie z. b. Kerberos, erfordern einen korrekten Server Prinzipal Namen für jede beliebige authentifizierte Sitzung. Ein Prinzipal ist eine Entität, die vom Sicherheitssystem erkannt wird. Dies schließt sowohl menschliche Benutzer als auch Systemdienste ein. Alle Prinzipal Namen haben ein ähnliches Format für eine bestimmte Security Support Provider (SSP). Ein SSP ist ein Softwaremodul, das die Sicherheitsüberprüfung ausführt. Weitere Informationen finden Sie unter [Übersicht über die SSPI-Architektur](sspi-architectural-overview.md). Um die Einheitlichkeit aufrechtzuerhalten, gibt ein Sicherheitsanbieter in der Regelsystem Dienste ähnliche Namen wie Benutzer. Unter einigen Sicherheitsanbietern haben Systemdienste möglicherweise keinen Prinzipal Namen.

Der Server registriert seinen Prinzipal Namen für den Sicherheitsanbieter mithilfe der [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion. Für jeden Sicherheitsanbieter kann nur ein Server Prinzipal Name verwendet werden. Wenn mehr als ein Name registriert ist, wird ein Name nach dem Zufallsprinzip ausgewählt und verwendet. Der SSP schreibt das Format des Prinzipal namens vor. Beispielsweise sehen die Kerberos/Aushandlungs-SSPs für einen Systemdienst ungefähr wie folgt aus: Computer \_ Name $ @childdomain.parentdomain1.parentdomain2.COM .

Die empfohlene Vorgehensweise zum Erstellen von Prinzipal Namen ist die Verwendung von dokumentierten APIs (z. b. der **dsmakespn** -Funktion), anstatt den Prinzipal Namen aus Zeichen folgen zu erstellen. Die Verwendung dokumentierter APIs steigert die Portabilität zwischen verschiedenen Bereitstellungs Umgebungen und beseitigt die Möglichkeit von Fehlern.

Durch die Angabe eines falschen Prinzipal namens kann verhindert werden, dass der Client und der Server eine authentifizierte Sitzung einrichten. Der Schannel-SSP übernimmt Prinzipal Namen in einer von zwei Formen:

-   Das erste SChannel-Prinzipal namens Formular ist das [*msstd*](m-glos.md) -Formular. Namen in msstd-Form folgen im Allgemeinen dem Muster msstd:servername@serverdomain.com . Dies wird als e-Mail-Name-Eigenschaft bezeichnet. Wenn das Zertifikat eine e-Mail-Name-Eigenschaft enthält und das @-Zeichen (@) enthält, lautet der Prinzipal Name msstd: Email Name. Andernfalls muss Sie die Common Name-Eigenschaft enthalten. Interne umgekehrte Schrägstriche werden wie bei Zeichen folgen Bindungen verdoppelt.
-   Das zweite SChannel-Prinzipal namens Formular ist das [*voll Text*](f-glos.md) Format. Dabei handelt es sich um eine Reihe von RFC1779-kompatiblen Namen, die durch eckige Klammern begrenzt und durch umgekehrte Schrägstriche voneinander getrennt sind. Sie folgt normalerweise dem Muster fullsic: \\ < \\ Authority \\ subauthority \\ .... \\ Person> oder fullsic: \\ < \\ Authority- \\ unter Autorität \\ ..... \\ Serverprogram->.

Wenn der Name nicht mit dem Zertifikat identisch ist, wird die Fehlermeldung " \_ Zugriff \_ verweigert" zurückgegeben. Wenn das Namensformat ungültig ist, gibt Schannel SSP den \_ ungültigen Code Fehler \_ Parameter zurück.

Um den Prinzipal Namen des Servers abzufragen, können Anwendungen [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)aufruft. Dadurch wird eine NULL-terminierte Zeichenfolge für den Prinzipal Namen zugewiesen. Bevor die Anwendung beendet wird, muss Sie [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) aufrufen, um den von dieser Zeichenfolge belegten Arbeitsspeicher freizugeben.

Das Abfragen des Server namens auf diese Weise ist nicht sicher und sollte vermieden werden. Bei der Server Authentifizierung sollte das Client Programm wissen, mit welchem Server es eine Verbindung herstellt, und den Server Prinzipal Namen neu erstellen.

 

 





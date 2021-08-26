---
title: Suchen von Endpunkten
description: Serverprogramme lauschen auf Endpunkte für Clientanforderungen. Die Syntax der Endpunktzeichenfolge hängt von der protokollfolge ab, die Sie verwenden. Beispielsweise ist der Endpunkt für TCP/IP eine Portnummer, und die Endpunktsyntax für Named Pipes ist ein gültiger Pipename.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024a85704287db7e5f78bb67eee9b64a7c6dc84ce5724623450d36f743e5fa9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021280"
---
# <a name="finding-endpoints"></a>Suchen von Endpunkten

Serverprogramme lauschen auf Endpunkte für Clientanforderungen. Die Syntax der Endpunktzeichenfolge hängt von der protokollfolge ab, die Sie verwenden. Beispielsweise ist der Endpunkt für TCP/IP eine Portnummer, und die Endpunktsyntax für Named Pipes ist ein gültiger Pipename.

Es gibt zwei Arten von Endpunkten: bekannte und dynamische Endpunkte. Die Wahl des Endpunkttyps, den Ihr Programm verwendet, bestimmt, ob die verteilte Anwendung oder die Laufzeitbibliothek den Endpunkt angibt.

In diesem Abschnitt werden Endpunkte erläutert und Informationen dazu angezeigt, wie sie zu finden sind. Sie ist in die folgenden Themen organisiert:

-   [Verwenden Well-Known Endpunkten](#using-well-known-endpoints)
-   [Verwenden dynamischer Endpunkte](#using-dynamic-endpoints)
-   [Exportieren Well-Known Endpunkte in die Endpunktzuordnungsdatenbank](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Die Begriffe *statische Endpunkte* und *bekannte* Endpunkte sind gleichwertig und werden austauschbar verwendet.

 

Es ist möglich, dass Ihre Clientanwendung die Endpunktzuordnung verwendet, um zu bestimmen, ob derzeit ein Serverprogramm ausgeführt wird. Ihr Client kann [**RpcMgmtInqIfIds,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids) [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)und [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) aufrufen, um zu sehen, ob der Server die bestimmte Schnittstelle registriert hat, die er in der Endpunktzuordnung benötigt.

## <a name="using-well-known-endpoints"></a>Verwenden bekannter Endpunkte

Bekannte Endpunkte sind vorab zugewiesene Endpunkte, die das Serverprogramm jedes Mal verwendet, wenn es ausgeführt wird. Da der Server immer auf diesen bestimmten Endpunkt lausiert, versucht der Client immer, eine Verbindung mit ihm herzustellen. Bekannte Endpunkte werden in der Regel von der für das Transportprotokoll zuständigen Stelle zugewiesen. Da Serverhostcomputer über eine begrenzte Anzahl verfügbarer Endpunkte verfügen, wird Anwendungsentwicklern dringend davon abgeraten, bekannte Endpunkte zu verwenden. Ein weiterer Vorteil dynamischer Endpunkte ist, dass sie die langfristige Verwaltung und Wartung des Systems vereinfachen.

Eine verteilte Anwendung kann einen bekannten Endpunkt in einer Zeichenfolge angeben und diese Zeichenfolge als Parameter an die [**Funktion RpcServerUseProtseqEp übergeben.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) Alternativ kann die Endpunktzeichenfolge im IDL-Dateischnittstellenheader als Teil des Endpunktschnittstellenattributs \[ [](/windows/desktop/Midl/endpoint) \] angezeigt werden.

Sie können zwei Ansätze verwenden, um den bekannten Endpunkt zu implementieren:

-   Angeben aller Informationen in einer Zeichenfolgenbindung
-   Store des bekannten Endpunkts in der Namensdienstdatenbank

Sie können alle Informationen schreiben, die erforderlich sind, um eine Bindung in eine verteilte Anwendung zu erstellen, wenn Sie sie entwickeln. Der Client kann den bekannten Endpunkt direkt in einer Zeichenfolge angeben, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) aufrufen, um eine Zeichenfolge zu erstellen, die alle Bindungsinformationen enthält, und diese Zeichenfolge an die [**Funktion RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) übergeben, um ein Handle zu erhalten. Client und Server können hart codiert werden, um einen bekannten Endpunkt zu verwenden, oder so geschrieben werden, dass die Endpunktinformationen von der Befehlszeile, einer Datendatei, einer Konfigurationsdatei oder der IDL-Datei stammen.

Ihre Clientanwendung kann auch eine Namensdienstdatenbank nach bekannten Endpunktinformationen abfragen.

## <a name="using-dynamic-endpoints"></a>Verwenden dynamischer Endpunkte

Die Anzahl der Endpunkte für einen bestimmten Server und eine bestimmte Protokollsequenz ist in der Regel begrenzt. Wenn Sie beispielsweise die [ncacn \_ ip \_ tcp-Protokollsequenz](/windows/desktop/Midl/ncacn-ip-tcp) verwenden, die angibt, dass die RPC-Netzwerkkommunikation über TCP/IP erfolgt, ist nur eine begrenzte Anzahl von Ports verfügbar (für die meisten Systeme ist nur der Bereich 1025 bis 5000 geöffnet). Mit den RPC-Laufzeitbibliotheken können Sie Endpunkte bei Bedarf dynamisch zuweisen. Da die Anzahl der möglichen Schnittstellen-UUIDs praktisch unbegrenzt ist, bietet die Verwendung der Schnittstellen-UUID zum Anführungszeichen des Aufrufs mehr Platz für Erweiterung und mehr Flexibilität.

Standardmäßig suchen die RPC-Laufzeitbibliotheksfunktionen nach Endpunktinformationen, wenn sie eine Namensdienstdatenbank abfragen. Wenn der Endpunkt dynamisch ist, enthält die Name-Dienstdatenbank keine Endpunktinformationen. Die Abfrage gibt Ihrem Clientprogramm jedoch den Namen eines Servers. Anschließend kann die Endpunktzuordnung des Servers durchsucht werden.

Wenn der Client einen Remoteprozeduraufruf mithilfe eines dynamischen Endpunkts erstellen muss, ist die bevorzugte Methode, den Aufruf für ein teilweise gebundenes Bindungshand handle zu erstellen. Die RPC-Laufzeit löst den Endpunkt transparent auf. Diese Methode ist der Verwendung der [**RpcEpResolveBinding-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) überlegen, da sie erweiterte Cachemechanismen in der RPC-Laufzeit zulässt.

Wenn eine spezifischere Steuerung der Endpunktauswahl erforderlich ist, können Clients die Endpunktzuordnung nach einem Eintrag nach der anderen durchsuchen, indem sie die [**Funktionen RpcMgmtEpEltInqBegin,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin) [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)und [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) aufrufen.

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportieren bekannter Endpunkte in die Endpunktzuordnungsdatenbank

Es ist möglich, die beiden Ansätze zum Suchen von Endpunkten zu kombinieren, insbesondere wenn ein verteiltes System von einem bekannten Endpunktmodell zu einem dynamischen Endpunktmodell übergewechselt wird. In solchen Übergängen verwendet eine Zwischenversion des Servers einen bekannten Endpunkt, registriert aber auch den bekannten Endpunkt bei der Endpunktzuordnungsdatenbank. Dieser Ansatz ermöglicht Clients, die einen bekannten Endpunkt verwenden, und Clients, die einen dynamischen Endpunkt verwenden, um eine Verbindung herzustellen. Nachdem alle Server aktualisiert wurden, kann eine neue Clientversion bereitgestellt werden, die nur dynamische Endpunkte verwendet. Nachdem alle Clients aktualisiert wurden, kann eine endgültige Serverversion die Verwendung bekannter Endpunkte beenden und nur mit der Verwendung dynamischer Endpunkte beginnen.

Dieser Ansatz ermöglicht einen Übergangspfad für Anwendungen, die mit einem bekannten Endpunkt gestartet wurden, aber zu einem dynamischen Endpunkt migrieren möchten, ohne dass ein gleichzeitiges Update aller Server und Clients erforderlich ist.

 

 
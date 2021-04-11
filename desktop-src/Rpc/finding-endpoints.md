---
title: Suchen von Endpunkten
description: Server Programme lauschen an Endpunkten für Client Anforderungen. Die Syntax der Endpunkt Zeichenfolge hängt von der verwendeten Protokoll Sequenz ab. Beispielsweise ist der Endpunkt für TCP/IP eine Portnummer, und die Endpunkt Syntax für Named Pipes ist ein gültiger Pipename.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0a97df3408a4d3c24dff9de28553f9e4b2210d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315368"
---
# <a name="finding-endpoints"></a>Suchen von Endpunkten

Server Programme lauschen an Endpunkten für Client Anforderungen. Die Syntax der Endpunkt Zeichenfolge hängt von der verwendeten Protokoll Sequenz ab. Beispielsweise ist der Endpunkt für TCP/IP eine Portnummer, und die Endpunkt Syntax für Named Pipes ist ein gültiger Pipename.

Es gibt zwei Typen von Endpunkten: bekannt und dynamisch. Welche Art von Endpunkt das Programm verwendet, bestimmt, ob die verteilte Anwendung oder die Lauf Zeit Bibliothek den Endpunkt angibt.

In diesem Abschnitt werden Endpunkte erläutert und Informationen dazu angezeigt, wie Sie gefunden werden. Es ist in die folgenden Themen unterteilt:

-   [Verwenden von Well-Known-Endpunkten](#using-well-known-endpoints)
-   [Verwenden dynamischer Endpunkte](#using-dynamic-endpoints)
-   [Exportieren von Well-Known Endpunkten in die Datenbank "Endpoint Map"](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Die Begriffe *statische Endpunkte* und *bekannte Endpunkte* sind gleichwertig und austauschbar.

 

Es ist möglich, dass Ihre Client Anwendung die Endpunkt Zuordnung verwendet, um zu bestimmen, ob ein Serverprogramm derzeit ausgeführt wird. Der Client kann [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)und [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) aufzurufen, um festzustellen, ob der Server die jeweilige Schnittstelle registriert hat, die er in der Endpunkt Zuordnung benötigt.

## <a name="using-well-known-endpoints"></a>Verwenden bekannter Endpunkte

Bekannte Endpunkte sind vorab zugewiesene Endpunkte, die vom Serverprogramm jedes Mal verwendet werden, wenn es ausgeführt wird. Da der Server immer auf diesen bestimmten Endpunkt lauscht, versucht der Client immer, eine Verbindung mit ihm herzustellen. Bekannte Endpunkte werden in der Regel von der Autorität zugewiesen, die für das Transportprotokoll zuständig ist. Da Server Host Computer über eine begrenzte Anzahl verfügbarer Endpunkte verfügen, wird dringend davon abgeraten, bekannte Endpunkte zu verwenden. Ein weiterer Vorteil dynamischer Endpunkte besteht darin, dass Sie die langfristige Verwaltung und Wartung des Systems vereinfachen.

Eine verteilte Anwendung kann einen bekannten Endpunkt in einer Zeichenfolge angeben und diese Zeichenfolge als Parameter an die Funktion [**rpcserveruseprotseqep**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)übergeben. Alternativ kann die Endpunkt Zeichenfolge im IDL-Datei Schnittstellen Header als Teil des \[ [](/windows/desktop/Midl/endpoint) \] Attributs der Endpunkt Schnittstelle angezeigt werden.

Sie können zwei Ansätze verwenden, um den bekannten Endpunkt zu implementieren:

-   Alle Informationen in einer Zeichen folgen Bindung angeben
-   Speichert den bekannten Endpunkt in der Name Service-Datenbank.

Sie können alle Informationen schreiben, die erforderlich sind, um eine Bindung in eine verteilte Anwendung zu erstellen, wenn Sie Sie entwickeln. Der Client kann den bekannten Endpunkt direkt in einer Zeichenfolge angeben, [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) aufrufen, um eine Zeichenfolge zu erstellen, die alle Bindungs Informationen enthält, und diese Zeichenfolge an die Funktion [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) übergeben, um ein Handle zu erhalten. Der Client und der Server können hart codiert werden, um einen bekannten Endpunkt zu verwenden, oder so geschrieben, dass die Endpunkt Informationen von der Befehlszeile, einer Datendatei, einer Konfigurationsdatei oder der IDL-Datei stammen.

Die Client Anwendung kann auch eine Name Service-Datenbank nach bekannten Endpunkt Informationen Abfragen.

## <a name="using-dynamic-endpoints"></a>Verwenden dynamischer Endpunkte

Die Anzahl der Endpunkte für einen bestimmten Server und eine bestimmte Protokoll Sequenz ist normalerweise eingeschränkt. Wenn Sie z. b. die [ncacn \_ IP- \_ TCP-](/windows/desktop/Midl/ncacn-ip-tcp) Protokoll Sequenz verwenden, die anzeigt, dass die RPC-Netzwerkkommunikation mithilfe von TCP/IP erfolgt, ist nur eine begrenzte Anzahl von Ports verfügbar (die meisten Systeme verfügen nur über den Bereich 1025 bis 5000 geöffnet). Mit den RPC-Laufzeitbibliotheken können Sie Endpunkte nach Bedarf dynamisch zuweisen. Da die Anzahl der möglichen Schnittstellen-UUIDs praktisch unbegrenzt ist, bietet die Verwendung der Interface UUID zur Weiterleitung des Aufrufes mehr Raum für die Erweiterung und mehr Flexibilität.

Standardmäßig suchen die Funktionen der RPC-Lauf Zeit Bibliothek nach Endpunkt Informationen, wenn Sie eine Name Service-Datenbank Abfragen. Wenn der Endpunkt dynamisch ist, enthält die Name Service-Datenbank keine Endpunkt Informationen. Die Abfrage gibt jedoch Ihrem Client Programm den Namen eines Servers. Anschließend kann die Endpunkt Zuordnung des Servers durchsucht werden.

Wenn der Client einen Remote Prozedur Aufrufvorgang mithilfe eines dynamischen Endpunkts ausführen muss, besteht die bevorzugte Methode darin, den-Befehl für ein teilweise gebundenes Bindungs handle auszuführen. Die RPC-Laufzeit löst den Endpunkt transparent auf. Diese Methode ist für die Verwendung der Funktion [**rpcepresolvebinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) besser, da Sie in der RPC-Laufzeit erweiterte zwischen Speicherungs Mechanismen zulässt.

Wenn eine genauere Steuerung der Endpunkt Auswahl erforderlich ist, können Clients die Endpunkt Zuordnung nacheinander durch Aufrufen der [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)-, [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)-und [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) -Funktionen durchsuchen.

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportieren von bekannten Endpunkten in die Datenbank der Endpunkt Zuordnung

Es ist möglich, die beiden Ansätze zum Ermitteln von Endpunkten zu mischen, insbesondere wenn ein verteiltes System von einem bekannten Endpunkt Modell in ein dynamisches Endpunkt Modell übergeht. Bei solchen Übergängen wird für eine zwischen Version des Servers ein bekannter Endpunkt verwendet, aber auch der bekannte Endpunkt wird bei der Datenbank der Endpunkt Zuordnung registriert. Dieser Ansatz ermöglicht es Clients, die bekannte Endpunkte und Clients verwenden, die einen dynamischen Endpunkt verwenden, um eine Verbindung herzustellen. Nachdem alle Server aktualisiert wurden, kann eine neue Client Version bereitgestellt werden, die nur dynamische Endpunkte verwendet. Nachdem alle Clients aktualisiert wurden, kann die endgültige Server Version die Verwendung bekannter Endpunkte nicht mehr unterbinden und nur dynamische Endpunkte verwenden.

Dieser Ansatz ermöglicht einen Übergangs Pfad für Anwendungen, die mit einem bekannten Endpunkt gestartet wurden, aber zu einem dynamischen Endpunkt migrieren möchten, ohne dass ein gleichzeitiges Update aller Server und Clients erforderlich ist.

 

 
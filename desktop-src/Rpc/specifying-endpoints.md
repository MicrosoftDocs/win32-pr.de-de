---
title: Angeben von Endpunkten
description: Angeben bekannter und dynamischer Endpunkte in Remote Prozedur Aufruf (RPC).
ms.assetid: fc39b527-11e6-45a7-b3b5-8bcf469633d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 373fb2818dd14670f5a939aa524c81fcdb05e20b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337242"
---
# <a name="specifying-endpoints"></a>Angeben von Endpunkten

Ein Endpunkt ist eine Netzwerk spezifische Adresse eines Server Prozesses für Remote Prozedur Aufrufe. Der tatsächliche Name des Endpunkts hängt von der verwendeten Protokoll Sequenz ab. Zum Beispiel TCP-, UDP-und http-verwendsports. Named Pipes verwendet einen Named Pipe Namen. Client/Server-Anwendungen können einen bekannten Endpunkt oder einen dynamischen Endpunkt verwenden. In diesem Abschnitt werden die Techniken vorgestellt, die von Serverprogrammen zum angeben bekannter und dynamischer Endpunkte verwendet werden. Diese Informationen werden in den folgenden Themen erläutert:

-   [Angeben von bekannten Endpunkten](#specifying-well-known-endpoints)
-   [Angeben dynamischer Endpunkte](#specifying-dynamic-endpoints)

## <a name="specifying-well-known-endpoints"></a>Angeben von bekannten Endpunkten

Wenn Ihr Server einen bekannten Endpunkt verwendet, kann er die Endpunkt Daten als Teil des Namensdienst-Daten Bank Eintrags einschließen. Wenn dies der Fall ist, enthält das Bindungs Handle des Clients eine komplette Server Adresse, die den bekannten Endpunkt enthält, wenn der Client das Bindungs Handle aus dem Server Eintrag importiert.

Mit dem Serverprogramm können auch bekannte Endpunkte angegeben werden, wenn die Protokoll Sequenzen angegeben werden. Rufen Sie entweder die Funktion [**rpcserveruseprotsetqep**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) oder [**rpcserveruseprotabqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) auf. Der Unterschied zwischen den beiden besteht darin, dass die letztere Funktion über einen zusätzlichen Parameter verfügt, den der Server verwenden kann, um die dynamische Port Zuweisung zu steuern.

Wenn Ihr Serverprogramm seine Endpunkt Informationen auf diese Weise angibt, sollte auch die [**rpcepregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) -Funktion aufgerufen werden, um den Endpunkt in der Endpunkt Zuordnung zu registrieren. Obwohl der Endpunkt immer identisch ist, kann der Client die Endpunkt Zuordnung verwenden, um nach dem Server zu suchen.

Wie Protokoll Sequenzen kann eine Anwendung Endpunkt Informationen in der IDL-Datei angeben. Wenn dies der Fall ist, sollte die Protokoll Sequenzen und die Endpunkte gleichzeitig registriert werden, indem die [**rpcserveruseallprotsqsif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) -oder [**rpcserveruseallprotsqsifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) -Funktion aufgerufen wird. In diesem Fall hat der Client Zugriff auf die Endpunkt Informationen über die Schnittstellen Spezifikation in der IDL-Datei. Daher ist es nicht erforderlich, die [**rpcepregiester**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) -Funktion aufzurufen.

## <a name="specifying-dynamic-endpoints"></a>Angeben dynamischer Endpunkte

Ein dynamischer Endpunkt ist ein Endpunkt, den der Server Host Computer zuweist, wenn der Server die Ausführung startet. Die meisten Server Anwendungen verwenden dynamische Endpunkte, um Konflikte mit anderen Programmen über die begrenzte Anzahl von Ports zu vermeiden, die auf dem Server Host-Computersystem verfügbar sind. Programme, die Named Pipes oder die [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) -Protokoll Sequenz verwenden, verfügen jedoch über einen sehr großen Endpunkt namens Bereich. Sie profitieren weniger von dynamischen Endpunkten als Programme, die andere Transporte verwenden.

Server Programme registrieren dynamische Endpunkte in einer Endpunkt Übersichts Datenbank. Wenn Sie möchten, dass der Server einen beliebigen verfügbaren Endpunkt verwendet, müssen Sie [**rpcserveruseallprotabqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**rpcserveruseallprotsqsex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex), [**rpcserveruseprotabf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) oder [**rpcserveruseprotabsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)aufrufen. Dadurch wird die RPC-Lauf Zeit Bibliothek so festgelegt, dass alle oder nur eine gültige Protokoll Sequenz mit dynamischen Endpunkten verwendet wird. Der Server sollte dann [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) aufgerufen werden, um einen Satz gültiger Bindungs Handles zu erhalten. Der Server übergibt den Satz von Bindungs Handles oder Bindungs Vektor an die Funktion [**rpcepregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , um alle geeigneten Endpunkte in der Endpunkt Zuordnung zu registrieren. Für jeden aufrufen, den der Server an **rpcepregiester** sendet, sollte ein entsprechender [**rpcbindingvectorfree-Befehl**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) vorhanden sein, um den vom Bindungs Vektor verwendeten Arbeitsspeicher freizugeben.

Beachten Sie, dass Serverprogramme die Funktion [**rpcepregisternoreplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) anstelle von [**rpcepregiester**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)verwenden können. Programme verwenden normalerweise **rpcepregisternoreplace** , wenn mehrere Kopien eines Server Programms auf einem Server Host System ausgeführt werden müssen.

Die Funktionen [**rpcepregisterund**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) [**rpcepregisternoreplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) fügen der Endpunkt-Mapper-Datenbank die Schnittstellen und Bindungs Handles des Servers hinzu. Wenn der Client einen Remote Prozedur Aufruf mithilfe eines teilweise gebundenen Handles ausführt, fordert die Lauf Zeit Bibliothek des Servers die Endpunkt Zuordnung des Server Computers zum Endpunkt einer kompatiblen Serverinstanz an. Die-Client Bibliothek stellt die-Schnittstelle (UUID), die Protokoll Sequenz und ggf. die Objekt-UUID im Client Bindungs Handle bereit. Der Endpunkt Mapper sucht nach einem Datenbankeintrag, der mit den Informationen des Clients übereinstimmt. Die UUID der Client/Server-Schnittstelle, die Hauptversion der Schnittstelle und die Protokoll Sequenz müssen genau übereinstimmen. Außerdem muss die neben Version der-Schnittstelle des Servers größer oder gleich der neben Version des Clients sein.

Wenn alle Tests erfolgreich sind, gibt die Endpunkt Zuordnung den gültigen Endpunkt zurück, und die Client Lauf Zeit Bibliothek aktualisiert den Endpunkt im Bindungs handle.

Dynamische Endpunkte werden automatisch aus der Endpunkt-Mapper-Datenbank gelöscht, wenn der Server Prozess nicht mehr ausgeführt wird. Sie können den Endpunkt entweder aus der Endpunkt-Mapper-Datenbank entfernen, bevor das Serverprogramm mit der [**rpcepunregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepunregister) -Funktion beendet wird, oder Sie können die automatische Bereinigung zum Verwalten des Entfernens des Endpunkts zulassen.

 

 
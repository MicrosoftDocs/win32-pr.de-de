---
title: Auffinden von Server Host Systemen
description: Auffinden von Server Hostsystemen mithilfe von Zeichen folgen Bindungen und durch Abfragen einer Name Service-Datenbank für den Speicherort eines Server Programms.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856299"
---
# <a name="finding-server-host-systems"></a>Auffinden von Server Host Systemen

Bei einem Server Host System handelt es sich um den Computer, auf dem das Serverprogramm der verteilten Anwendung ausgeführt wird. Es gibt möglicherweise ein oder mehrere Server Host Systeme in einem Netzwerk. Wie das Client Programm einen Server findet, zu dem eine Verbindung hergestellt werden soll, hängt von den Anforderungen des Programms ab.

Es gibt zwei Methoden zum Auffinden von Server Hostsystemen:

-   Verwendung von Informationen, die in Zeichen folgen im Client Quellcode, in Umgebungsvariablen oder in anwendungsspezifischen Konfigurationsdateien gespeichert sind. Die Client Anwendung kann die Daten in der Zeichenfolge verwenden, um eine Bindung zwischen dem Client und dem Server zu erstellen.
-   Abfragen einer Name Service-Datenbank für den Speicherort eines Server Programms.

Dieser Abschnitt enthält Informationen zu diesen beiden Techniken in den folgenden Themen:

-   [Verwenden von Zeichen folgen Bindungen](#using-string-bindings)
-   [Importieren aus Name Service-Datenbanken](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Verwenden von Zeichen folgen Bindungen

Anwendungen können Bindungen aus Informationen erstellen, die in Zeichen folgen gespeichert werden. Ihre Client Anwendung verfasst diese Informationen als Zeichenfolge und ruft dann die [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) -Funktion auf. Der Client muss die folgenden Informationen bereitstellen, um den Server zu identifizieren:

-   Der Schnittstellen Name, der Globally Unique Identifier (GUID) des Objekts oder die UUID des Objekts. Weitere Informationen finden Sie unter [generierende Schnittstelle UUIDs](generating-interface-uuids.md) und [Zeichenfolge UUID](string-uuid.md).
-   Der Transporttyp, über den kommuniziert werden soll, z. b. Named Pipes oder TCP/IP. Weitere Informationen finden Sie unter [wichtige RPC-Bindungs Begriffe](essential-rpc-binding-terminology.md) und [Auswählen einer Protokoll Sequenz](selecting-a-protocol-sequence.md).
-   Die Netzwerkadresse oder der Name des Server Host Computers.
-   Der Endpunkt des Server Programms auf dem Server Host Computer. Weitere Informationen finden Sie untersuchen von [Endpunkten](finding-endpoints.md)und [Angeben von Endpunkten](specifying-endpoints.md).

(Die Objekt-UUID und die Endpunkt Informationen sind optional.)

In den folgenden Beispielen enthalten der *psznetworkaddress* -Parameter und andere Parameter eingebettete umgekehrte Schrägstriche. Der umgekehrte Schrägstrich ist ein Escapezeichen in der Programmiersprache C. Zwei umgekehrte Schrägstriche sind erforderlich, um jeden einzelnen literalen umgekehrten Schrägstrich darzustellen. Die Zeichen folgen Bindungsstruktur muss vier umgekehrte Schrägstriche enthalten, um die beiden literalen umgekehrten Schrägstriche zu repräsentieren, die dem Servernamen vorangestellt sind.

Das folgende Beispiel zeigt, dass dem Servernamen acht umgekehrte Schrägstriche vorangestellt werden müssen, damit vier literale umgekehrte Schrägstriche in der Datenstruktur für die Zeichen folgen Bindung angezeigt werden, nachdem die **sprintf \_ s** -Funktion die Zeichenfolge verarbeitet hat.


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



Im folgenden Beispiel wird die Zeichen folgen Bindung folgendermaßen angezeigt:

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *Servername* \[ \\ \\ Pipe \\ \\ *Pipename*\]

Der Client ruft dann [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um das Bindungs Handle abzurufen:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Eine Hilfsfunktion, [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) , assembliert das Objekt UUID, die Protokoll Sequenz, die Netzwerkadresse und den Endpunkt in der korrekten Syntax für den Aufrufen von [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding). Sie müssen sich keine Gedanken darüber machen, wie Sie das kaufmännische und-Doppelpunkte sowie die verschiedenen Komponenten für jede Protokoll Sequenz an der richtigen Stelle platzieren. die Zeichen folgen werden lediglich als Parameter für die Funktion bereitgestellt. Die Lauf Zeit Bibliothek weist sogar den für die Zeichen folgen Bindung benötigten Arbeitsspeicher zu.


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



Eine andere Hilfsfunktion, [**rpcbindingtostringbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), übernimmt ein Bindungs Handle als Eingabe und erzeugt die entsprechende Zeichen folgen Bindung.

## <a name="importing-from-name-service-databases"></a>Importieren aus Name Service-Datenbanken

Name Dienst Datenbanken speichern unter anderem Bindungs Handles und UUIDs. Die Client Anwendung kann nach einer oder beiden von Ihnen suchen, wenn Sie an den Server gebunden werden muss. Eine Erläuterung der Informationen, die von einem Namensdienst gespeichert werden, und des Speicher Formats finden Sie [unter RPC Name Service Database](the-rpc-name-service-database.md).

Die RPC-Bibliothek stellt zwei Funktions Sätze bereit, mit denen das Client Programm die Name Service-Datenbank durchsuchen kann. Die Namen eines Satzes beginnen mit rpcnsbindingimport. Die Namen der anderen Gruppe beginnen mit rpcnsbindinglookup. Der Unterschied zwischen den beiden Gruppen von Funktionen besteht darin, dass die rpcnsbindingimport-Funktionen ein einzelnes Bindungs handle pro Rückruf zurückgeben und die rpcnsbindinglookup-Funktionen Gruppen von Handles pro Rückruf zurückgeben.

Um eine Suche mit den rpcnsbindingimport-Funktionen zu starten, müssen Sie zuerst [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)aufrufen, wie im folgenden Code Fragment gezeigt.


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



Wenn die RPC-Funktionen die Name Service-Datenbank durchsuchen, benötigen Sie einen Platz, um die Suche zu starten. In der RPC-Terminologie wird dies als Eintrags Name bezeichnet. Das Client Programm übergibt den Namen des Eintrags als zweiten Parameter an [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Dieser Parameter kann **null** sein, wenn Sie die gesamte Name Service-Datenbank durchsuchen möchten. Alternativ können Sie den Server Eintrag durchsuchen, indem Sie einen Server Eintrags Namen übergeben oder den Gruppen Eintrag durchsuchen, indem Sie einen Gruppen Eintrags Namen übergeben. Durch die Übergabe eines Eintrags namens wird die Suche auf den Inhalt dieses Eintrags beschränkt.

Im vorherigen Beispiel wird der Wert RPC \_ C \_ NS- \_ Syntax \_ Default als erster Parameter an [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)übergeben. Dadurch wird die standardmäßige Eingabe Namen Syntax ausgewählt. Derzeit ist dies die einzige unterstützte Eingabe namens Syntax.

Die Client Anwendung kann die Name Service-Datenbank nach einem Schnittstellennamen, einer UUID oder beidem durchsuchen. Wenn Sie eine Schnittstelle nach Namen suchen möchten, übergeben Sie die globale Schnittstellen Variable, die der mittlerer l-Compiler generiert, aus ihrer IDL-Datei als dritten Parameter an [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Sie finden die Deklaration in der Header Datei, die vom-compilercompiler beim Generieren des clientstubs generiert wurde. Wenn das Client Programm nur nach UUID suchen soll, legen Sie den dritten Parameter auf **null** fest.

Legen Sie beim Durchsuchen der Name Service-Datenbank nach einer UUID den vierten Parameter von [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) auf die UUID fest, nach der Sie suchen möchten. Wenn Sie nicht nach einer UUID suchen, legen Sie diesen Parameter auf **null** fest.

Die [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) -Funktion übergibt die Adresse eines Namensdienst – Such Kontext Handles über den fünften Parameter. Sie übergeben diesen Parameter an andere rpcnsbindingimport-Funktionen.

Die nächste Funktion, die von der Client Anwendung aufgerufen wird, ist " [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)". Client Programme verwenden diese Funktion zum Abrufen kompatibler Bindungs Handles aus der Name Service-Datenbank. Das folgende Code Fragment veranschaulicht, wie diese Funktion aufgerufen werden kann:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Nachdem die Funktion [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) zum Abrufen eines Bindungs Handles aufgerufen hat, kann Ihre Client Anwendung ermitteln, ob das empfangene handle akzeptabel ist. Andernfalls kann das Client Programm eine Schleife ausführen und **rpcnsbindingimportnext** erneut ausführen, um festzustellen, ob der Namensdienst ein geeignetere Handle enthält. Für jeden Aufrufen von **rpcnsbindingimportnext** muss ein entsprechender Aufrufen von rpcnsbindingfree vorhanden sein. Wenn die Suche abgeschlossen ist, können Sie die Funktion [**rpcnsbindingimportdone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) zum Freigeben des Such Kontexts abrufen.

Nachdem die Client Anwendung über ein akzeptables Bindungs Handle verfügt, sollte Sie sicherstellen, dass die Serveranwendung ausgeführt wird. Es gibt zwei Methoden, mit denen Ihr Client diese Überprüfung durchführen kann. Der erste besteht darin, eine Funktion in der Client Schnittstelle aufzurufen. Wenn das Serverprogramm ausgeführt wird, wird der-Vorgang beendet. Wenn dies nicht der Fall ist, tritt ein Fehler auf. Eine bessere Möglichkeit, um zu überprüfen, ob der Server ausgeführt wird, ist das Aufrufen von [**rpcepresolvebinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), gefolgt von einem Aufruf von [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Weitere Informationen zur Name Service-Datenbank finden Sie [unter RPC Name Service Database](the-rpc-name-service-database.md).

 

 





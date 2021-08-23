---
title: Suchen von Serverhostsystemen
description: Suchen von Serverhostsystemen mithilfe von Zeichenfolgenbindungen und Abfragen einer Namensdienstdatenbank nach dem Speicherort eines Serverprogramms.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180e2e43c0350f55defb74762d6ab1b6b656dafbc1468bcc7f077ed9780a2e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929989"
---
# <a name="finding-server-host-systems"></a>Suchen von Serverhostsystemen

Ein Serverhostsystem ist der Computer, auf dem das Serverprogramm der verteilten Anwendung ausgeführt wird. Es kann ein oder mehrere Serverhostsysteme in einem Netzwerk geben. Wie Ihr Clientprogramm einen Server findet, mit dem eine Verbindung hergestellt werden kann, hängt von den Anforderungen Ihres Programms ab.

Es gibt zwei Methoden zum Suchen von Serverhostsystemen:

-   Verwenden von Informationen, die in Zeichenfolgen im Client-Quellcode, umgebungsvariablen oder anwendungsspezifischen Konfigurationsdateien gespeichert sind. Ihre Clientanwendung kann die Daten in der Zeichenfolge verwenden, um eine Bindung zwischen dem Client und dem Server zu erstellen.
-   Abfragen einer Namensdienstdatenbank nach dem Speicherort eines Serverprogramms.

Dieser Abschnitt enthält Informationen zu diesen beiden Techniken in den folgenden Themen:

-   [Verwenden von Zeichenfolgenbindungen](#using-string-bindings)
-   [Importieren aus Name Service-Datenbanken](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Verwenden von Zeichenfolgenbindungen

Anwendungen können Bindungen aus Informationen erstellen, die in Zeichenfolgen gespeichert sind. Ihre Clientanwendung erstellt diese Informationen als Zeichenfolge und ruft dann die [**RpcBindingFromStringBinding-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf. Der Client muss die folgenden Informationen zur Identifizierung des Servers liefern:

-   Der Schnittstellenname, der GUID (Globally Unique Identifier) des Objekts oder die UUID des Objekts. Weitere Informationen finden Sie unter [Generieren von Schnittstellen-UUIDs](generating-interface-uuids.md) und [String UUID](string-uuid.md).
-   Der Transporttyp, über den kommuniziert werden soll, z. B. Named Pipes oder TCP/IP. Weitere Informationen finden Sie unter Essential RPC Binding Terminology (Grundlegende [RPC-Bindungsterminologie)](essential-rpc-binding-terminology.md) [und Auswählen einer Protokollsequenz](selecting-a-protocol-sequence.md).
-   Die Netzwerkadresse oder der Name des Serverhostcomputers.
-   Der Endpunkt des Serverprogramms auf dem Serverhostcomputer. Weitere Informationen finden Sie unter [Suchen von Endpunkten](finding-endpoints.md)und [Angeben von Endpunkten.](specifying-endpoints.md)

(Die Objekt-UUID und die Endpunktinformationen sind optional.)

In den folgenden Beispielen enthalten *der pszNetworkAddress-Parameter* und andere Parameter eingebettete schräge Schrägstriche. Der schräge Schrägstrich ist ein Escapezeichen in der Programmiersprache C. Zwei gegensätzlichen Schrägstriche sind erforderlich, um jedes einzelne literale schräge Schrägstrichzeichen zu darstellen. Die Zeichenfolgenbindungsstruktur muss vier schräge Schrägstriche enthalten, um die beiden literalen schrägen Schrägstriche vor dem Servernamen darstellen zu können.

Das folgende Beispiel zeigt, dass dem Servernamen acht schräge Schrägstriche vorangehende werden müssen, damit vier literale schräge Schrägstriche in der Datenstruktur mit Zeichenfolgenbindung angezeigt werden, nachdem die **Sprintf-Funktion \_** die Zeichenfolge verarbeitet hat.


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



Im folgenden Beispiel wird die Zeichenfolgenbindung wie folgt angezeigt:

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np: \\ \\ \\ \\ *servername* \[ \\ \\ pipe \\ \\ *pipename*\]

Der Client ruft dann [**RpcBindingFromStringBinding auf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) um das Bindungshand handle zu erhalten:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



[**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) stellt die Objekt-UUID, die Protokollsequenz, die Netzwerkadresse und den Endpunkt in der richtigen Syntax für den Aufruf von [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)zusammen. Sie müssen sich nicht darum kümmern, das ampersand, den Doppelpunkt und die verschiedenen Komponenten für jede Protokollsequenz an der richtigen Stelle zu platzieren. Sie geben die Zeichenfolgen nur als Parameter für die Funktion an. Die Laufzeitbibliothek weist sogar den Arbeitsspeicher zu, der für die Zeichenfolgenbindung benötigt wird.


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



Eine weitere Benutzerfunktion, [**RpcBindingToStringBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)verwendet ein Bindungshand handle als Eingabe und erzeugt die entsprechende Zeichenfolgenbindung.

## <a name="importing-from-name-service-databases"></a>Importieren aus Name Service-Datenbanken

Namensdienstdatenbanken speichern unter anderem Bindungshandles und UUIDs. Ihre Clientanwendung kann nach einer oder beiden suchen, wenn sie eine Bindung an den Server herstellen muss. Eine Erörterung der Informationen, die von einem Namensdienst gespeichert werden, und des Speicherformats finden Sie unter [Die RPC-Name-Dienstdatenbank](the-rpc-name-service-database.md).

Die RPC-Bibliothek stellt zwei Sätze von Funktionen zur Verfügung, mit denen Ihr Clientprogramm die Namensdienstdatenbank durchsuchen kann. Die Namen einer Gruppe beginnen mit RpcNsBindingImport. Die Namen der anderen Gruppe beginnen mit RpcNsBindingLookup. Der Unterschied zwischen den beiden Gruppen von Funktionen ist, dass die RpcNsBindingImport-Funktionen pro Aufruf ein einzelnes Bindungshandles zurückgeben und die RpcNsBindingLookup-Funktionen Gruppen von Handles pro Aufruf zurückgeben.

Um eine Suche mit den RpcNsBindingImport-Funktionen zu starten, rufen Sie zuerst [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)auf, wie im folgenden Codefragment gezeigt.


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



Wenn die RPC-Funktionen die Namensdienstdatenbank durchsuchen, benötigen sie einen Ort, um die Suche zu starten. In der RPC-Terminologie wird dies als Eintragsname bezeichnet. Ihr Clientprogramm übergibt den Eintragsnamen als zweiten Parameter an [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Dieser Parameter kann NULL **sein,** wenn Sie die gesamte Namensdienstdatenbank durchsuchen möchten. Alternativ können Sie den Servereintrag durchsuchen, indem Sie einen Servereintragsnamen übergeben oder den Gruppeneintrag durch Übergeben eines Gruppeneintragsnamens durchsuchen. Die Übergabe eines Eintragsnamens schränkt die Suche auf den Inhalt dieses Eintrags ein.

Im vorherigen Beispiel wird der Wert RPC C NS SYNTAX DEFAULT als erster Parameter an \_ \_ \_ \_ [**RpcNsBindingImportBegin übergeben.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Dadurch wird die Standardsyntax für den Eintragsnamen ausgewählt. Derzeit ist dies die einzige unterstützte Eingabenamensyntax.

Ihre Clientanwendung kann die Datenbank des Namensdiensts nach einem Schnittstellennamen, einer UUID oder beidem durchsuchen. Wenn Sie eine Schnittstelle nach Namen suchen möchten, übergeben Sie die globale Schnittstellenvariable, die der MIDL-Compiler aus Ihrer IDL-Datei generiert, als dritten Parameter an [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Sie finden die Deklaration in der Headerdatei, die der MIDL-Compiler generiert hat, als er den Clientstub generiert hat. Wenn Ihr Clientprogramm nur nach UUID suchen soll, legen Sie den dritten Parameter auf **NULL fest.**

Legen Sie beim Durchsuchen der Namensdienstdatenbank nach einer UUID den vierten Parameter von [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) auf die UUID fest, nach der Sie suchen möchten. Wenn Sie nicht nach einer UUID suchen, legen Sie diesen Parameter auf **NULL fest.**

Die [**RpcNsBindingImportBegin-Funktion**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) übergibt die Adresse eines Namensdienst-Suchkontexthandpunkts über ihren fünften Parameter. Sie übergeben diesen Parameter an andere RpcNsBindingImport-Funktionen.

Die nächste Funktion, die Ihre Clientanwendung aufrufen würde, ist [**insbesondere RpcNsBindingImportNext.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) Clientprogramme verwenden diese Funktion, um kompatible Bindungshandles aus der Namensdienstdatenbank abzurufen. Das folgende Codefragment veranschaulicht, wie diese Funktion aufgerufen werden kann:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Nachdem die [**RpcNsBindingImportNext-Funktion**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) aufgerufen wurde, um ein Bindungshand handle zu erhalten, kann Ihre Clientanwendung bestimmen, ob das empfangene Handle akzeptabel ist. Falls nicht, kann das Clientprogramm eine Schleife ausführen und **RpcNsBindingImportNext** erneut aufrufen, um zu sehen, ob der Name-Dienst ein geeigneteres Handle enthält. Für jeden Aufruf von **RpcNsBindingImportNext** muss ein entsprechender Aufruf von RpcNsBindingFree erfolgen. Rufen Sie nach Abschluss der Suche die [**Funktion RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) auf, um den Suchkontext frei zu geben.

Nachdem Ihre Clientanwendung über ein akzeptables Bindungshand handle verfügt, sollte sie überprüfen, ob die Serveranwendung ausgeführt wird. Es gibt zwei Methoden, die Ihr Client verwenden kann, um diese Überprüfung durchzuführen. Die erste besteht im Aufrufen einer Funktion in der Clientschnittstelle. Wenn das Serverprogramm ausgeführt wird, wird der Aufruf abgeschlossen. Wenn dies nicht der Fehler ist, kann der Aufruf nicht mehr werden. Eine bessere Möglichkeit, um zu überprüfen, ob der Server ausgeführt wird, ist das Aufrufen von [**RpcEpResolveBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding)gefolgt von einem Aufruf von [**RpcMgmtIsServerListening.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening) Weitere Informationen zur Datenbank des Namensdiensts finden Sie unter [The RPC Name Service Database](the-rpc-name-service-database.md).

 

 





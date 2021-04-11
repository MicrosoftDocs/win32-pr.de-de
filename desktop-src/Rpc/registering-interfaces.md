---
title: Registrieren von Schnittstellen
description: Registrieren einer Remote Prozedur Aufruf-Schnittstelle (RPC).
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea9e851e8c9663c8f66d983d3400b1ee398a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206235"
---
# <a name="registering-interfaces"></a>Registrieren von Schnittstellen

In diesem Abschnitt wird ausführlich erläutert, wie Sie eine RPC-Schnittstelle registrieren.

Die Informationen in diesem Abschnitt finden Sie in den folgenden Themen:

-   [Schnittstellen Registrierungsfunktionen](#interface-registration-functions)
-   [Einstiegspunkt Vektoren](#entry-point-vectors)
-   [Manager-EPVs](#manager-epvs)
-   [Registrieren einer einzelnen Implementierung einer Schnittstelle](#registering-a-single-implementation-of-an-interface)
-   [Registrieren mehrerer Implementierungen einer Schnittstelle](#registering-multiple-implementations-of-an-interface)
-   [Regeln zum Aufrufen von Manager-Routinen](#rules-for-invoking-manager-routines)
-   [Senden eines Remote Prozedur Aufrufes an eine Server-Manager Routine](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [Bereitstellen Ihrer eigenen Object-Inquiry-Funktion](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>Schnittstellen Registrierungsfunktionen

Server registrieren ihre Schnittstellen durch Aufrufen der Funktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) . Komplexe Serverprogramme unterstützen häufig mehr als eine Schnittstelle. Server Anwendungen müssen diese Funktion für jede Schnittstelle, die Sie unterstützen, einmal aufgerufen werden.

Außerdem können Server mehrere Versionen derselben Schnittstelle unterstützen, von denen jede über eine eigene Implementierung der Schnittstellen Funktionen verfügt. Wenn das Serverprogramm dies durchführt, muss es einen Satz von Einstiegspunkten bereitstellen. Ein Einstiegspunkt ist eine Manager-Routine, die Aufrufe für eine Version einer Schnittstelle sendet. Für jede Version der Schnittstelle muss ein Einstiegspunkt vorhanden sein. Die Gruppe der Einstiegspunkte wird als Einstiegspunkt Vektor bezeichnet. Weitere Informationen finden Sie unter [Einstiegspunkt Vektoren](#entry-point-vectors).

Zusätzlich zur Standardfunktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)unterstützt RPC auch andere Schnittstellen Registrierungsfunktionen. Die Funktion [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) erweitert die Funktionen von **RpcServerRegisterIf** , indem es Ihnen ermöglicht, einen Satz von Registrierungsflags (siehe [schnittstellenregistrierungs-Flags](interface-registration-flags.md)), die maximale Anzahl von gleichzeitigen Remote Prozedur aufrufen, die vom Server akzeptiert werden können, und die maximale Größe in Bytes eingehender Datenblöcke anzugeben.

Die RPC-Bibliothek enthält auch eine Funktion mit dem Namen " [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)". Wie die Funktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) registriert diese Funktion eine Schnittstelle. Das Serverprogramm kann diese Funktion auch verwenden, um einen Satz von Registrierungsflags (siehe [schnittstellenregistrierungs-Flags](interface-registration-flags.md)), die maximale Anzahl von gleichzeitigen Remote Prozedur Aufrufanforderungen, die der Server akzeptieren kann, und eine Sicherheits Rückruffunktion anzugeben.

Die Funktionen [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)und [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) legen Werte in der Registrierungs Tabelle der internen Schnittstelle fest. Diese Tabelle wird verwendet, um die Schnittstelle UUID und die Objekt-UUIDs einem Manager-EPV zuzuordnen. Der Manager-EPV ist ein Array von Funktions Zeigern, das genau einen Funktionszeiger für jeden Funktionsprototyp in der Schnittstelle enthält, die in der IDL-Datei angegeben ist.

Informationen zum Bereitstellen mehrerer EPVs zur Bereitstellung mehrerer Implementierungen der-Schnittstelle finden Sie unter [mehrere Schnittstellen Implementierungen](#registering-multiple-implementations-of-an-interface).

Die Lauf Zeit Bibliothek verwendet die Schnittstellen Registrierungs Tabelle (festgelegt durch Aufrufe der Funktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)) und die Objekt Registrierungs Tabelle (durch Aufrufe der Funktion [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)festgelegt), um dem Funktionszeiger Schnittstellen-und Objekt-UUIDs zuzuordnen.

Wenn Sie möchten, dass das Serverprogramm eine Schnittstelle aus der RPC-Lauf Zeit Bibliotheks Registrierung entfernt, müssen Sie die Funktion [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) aufrufen. Nachdem die Schnittstelle aus der Registrierung entfernt wurde, werden neue Aufrufe für diese Schnittstelle von der RPC-Lauf Zeit Bibliothek nicht mehr akzeptiert.

## <a name="entry-point-vectors"></a>Einstiegspunkt Vektoren

Der-Manager-Einstiegspunkt Vektor (EPV) ist ein Array von Funktions Zeigern, die auf Implementierungen der in der IDL-Datei angegebenen Funktionen verweisen. Die Anzahl der Elemente im Array entspricht der Anzahl von Funktionen, die in der IDL-Datei angegeben sind. RPC unterstützt mehrere Einstiegspunkt Vektoren, die mehrere Implementierungen der Funktionen darstellen, die in der-Schnittstelle angegeben sind.

Der mittlerer l-Compiler generiert automatisch einen Manager-EPV-Datentyp für die Erstellung von Manager-EPVs. Der-Datentyp hat den Namen * if-Name ***\_ Server \_ EPV**, wobei *if-Name* den Schnittstellen Bezeichner in der IDL-Datei angibt.

Der mittlerer l-Compiler erstellt und initialisiert automatisch einen Standard-Manager-EPV unter der Annahme, dass für jede Prozedur in der Schnittstelle eine Manager-Routine mit dem gleichen Namen vorhanden ist und in der IDL-Datei angegeben ist.

Wenn ein Server mehrere Implementierungen derselben Schnittstelle bietet, muss der Server für jede Implementierung einen zusätzlichen Manager-EPV erstellen. Jeder EPV muss genau einen Einstiegspunkt (Adresse einer Funktion) für jede Prozedur enthalten, die in der IDL-Datei definiert ist. Die Serveranwendung deklariert und Initialisiert eine-Manager-EPV-Variable vom Typ " *if-Name * * * \_ Server \_ EPV**" für jede zusätzliche Implementierung der-Schnittstelle. Um die EPVs zu registrieren, ruft Sie [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) Once für jeden unterstützten Objekttyp auf.

Wenn der Client einen Remote Prozedur Aufrufe an den Server ausführt, wird der EPV, der den Funktionszeiger enthält, basierend auf der Schnittstelle UUID und dem Objekttyp ausgewählt. Der Objekttyp wird von der Objekt-Abfragefunktion oder der durch [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)kontrollierten Tabellen gesteuerten Zuordnung abgeleitet.

## <a name="manager-epvs"></a>Manager-EPVs

Standardmäßig verwendet der mittlerer l-Compiler die Prozedur Namen aus der IDL-Datei einer Schnittstelle, um einen Manager-EPV zu generieren, den der Compiler direkt in den Serverstub platziert. Dieser Standard-EPV wird statisch mithilfe der in der Schnittstellen Definition deklarierten Prozedur Namen initialisiert.

Wenn Sie einen Vorgesetzten mit dem Standard-EPV registrieren möchten, geben Sie **null** als Wert des *mgrepv* -Parameters in einem Aufrufen der Funktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) an. Wenn die von einem Vorgesetzten verwendeten Routine Namen denen der Schnittstellen Definition entsprechen, können Sie diesen Manager mit dem Standard-EPV der vom Mittelwert Compiler generierten Schnittstelle registrieren. Sie können einen Vorgesetzten auch mit einem von der Serveranwendung bereitgestellten EPV registrieren.

Ein Server kann (und manchmal) einen nicht-**null** -Manager-EPV für eine Schnittstelle erstellen und registrieren. Übergeben Sie die Adresse eines EPV, dessen Wert vom Server als Wert des *mgrepv* a-Parameters deklariert wurde, um eine von der Serveranwendung – bereitgestellte EPV-Anwendung auszuwählen. Ein Wert ungleich **null** für den *mgrepv* -Parameter a überschreibt immer einen Standard-EPV im Server-Stub.

Der-Mittell-Compiler generiert automatisch einen-Manager-EPV-Datentyp (RPC \_ Mgr \_ EPV) für eine Serveranwendung, die beim Erstellen von Manager-EPVs verwendet werden soll. Ein Manager-EPV muss genau einen Einstiegspunkt (Funktions Adresse) für jede Prozedur enthalten, die in der IDL-Datei definiert ist.

Ein Server muss in den folgenden Fällen einen EPV ungleich **null** angeben:

-   Wenn sich die Namen der Manager-Routinen von den in der Schnittstellen Definition deklarierten Prozedur Namen unterscheiden
-   Wenn der Server den Standard-EPV zum Registrieren einer anderen Implementierung der-Schnittstelle verwendet

Ein Server deklariert einen Manager-EPV, indem er für jede Implementierung der Schnittstelle eine Variable vom Typ " *if-Name * * * \_ Server \_ EPV**" initialisiert.

## <a name="registering-a-single-implementation-of-an-interface"></a>Registrieren einer einzelnen Implementierung einer Schnittstelle

Wenn ein Server nur eine Implementierung einer Schnittstelle bietet, ruft der Server [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) nur einmal auf. Im Standardfall verwendet der Server den Standard-Manager-EPV. (Die Ausnahme ist, wenn der Manager Routine Namen verwendet, die sich von den in der-Schnittstelle deklarierten Namen unterscheiden.)

Für den Standardfall geben Sie die folgenden Werte für Aufrufe von [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)an:

-   Manager-EPVs

    Um den Standard-EPV zu verwenden, geben Sie einen **null** -Wert für den *mgrepv* a-Parameter an.

-   Manager-Typ UUID

    Wenn Sie den Standard-EPV verwenden, registrieren Sie die Schnittstelle mit einem Nil-Manager-Typ UUID, indem Sie einen **null** -Wert oder eine Nil-UUID für den *mgrtypeuuid* -Parameter angeben. In diesem Fall werden alle Remote Prozedur Aufrufe unabhängig von der Objekt-UUID in Ihrem Bindungs Handle an den Standard-EPV gesendet, wobei angenommen wird, dass keine [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Aufrufe durchgeführt wurden.

    Sie können auch einen nicht-Nil-Manager-Typ "uuid" angeben. In diesem Fall müssen Sie auch die [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine aufrufen.

## <a name="registering-multiple-implementations-of-an-interface"></a>Registrieren mehrerer Implementierungen einer Schnittstelle

Sie können mehr als eine Implementierung der in der IDL-Datei angegebenen remote Prozedur (en) bereitstellen. Die Serveranwendung ruft [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) auf, um dem Typ UUIDs Objekt-UUIDs zuzuordnen, und ruft [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) auf, um den Typ "uuid" von Manager EPVs zuzuordnen. Wenn ein Remote Prozedur Aufruf mit der Objekt-UUID eingeht, ordnet die RPC-Server Lauf Zeit Bibliothek das Objekt UUID einem Typ UUID zu. Die Serveranwendung verwendet dann den Typ "uuid" und die Schnittstelle "uuid", um den Manager-EPV auszuwählen.

Sie können auch eine eigene Funktion angeben, um die Zuordnung von Objekt UUID zum Manager-Typ UUID aufzulösen. Sie geben die Zuordnungs Funktion an, wenn Sie " [**rpcobjectsettinqfn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn)" aufrufen.

Zum Bereitstellen mehrerer Implementierungen einer Schnittstelle muss ein Server jede Implementierung durch Aufrufen von [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) separat registrieren. Für jede Implementierung, die ein Server registriert, liefert er denselben *ifspec* -Parameter, aber ein anderes Paar von *mgrtypeuuid* -und *mgrepv* -Parametern.

Verwenden Sie im Fall mehrerer Manager [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) wie folgt:

-   Manager-EPVs

    Zum anbieten mehrerer Implementierungen einer Schnittstelle muss ein Server folgende Aktionen ausführen:

    -   Erstellen Sie einen nicht-**null** -Manager-EPV für jede weitere Implementierung.
    -   Geben Sie einen Wert ungleich **null** für den *mgrepv* a-Parameter in [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)an.

    Beachten Sie, dass sich der Server auch beim Standard-Manager-EPV registrieren kann.

-   Manager-Typ UUID

    Stellen Sie für jeden EPV der Schnittstelle eine UUID für den Manager bereit. Der **Nulltyp** UUID (oder NULL-Wert) für den *mgrtypeuuid* -Parameter kann für einen der Manager-EPVs angegeben werden. Jeder Typ UUID muss anders sein.

## <a name="rules-for-invoking-manager-routines"></a>Regeln zum Aufrufen von Manager-Routinen

Die RPC-Lauf Zeit Bibliothek sendet einen eingehenden Remote Prozedur Aufruf an einen Vorgesetzten, der die angeforderte RPC-Schnittstelle anbietet. Wenn mehrere Manager für eine Schnittstelle registriert sind, muss von der RPC-Lauf Zeit Bibliothek eine ausgewählt werden. Zur Auswahl eines Vorgesetzten verwendet die RPC-Lauf Zeit Bibliothek die vom Bindungs Handle des Aufrufs angegebene Objekt-UUID.

Die Lauf Zeit Bibliothek wendet die folgenden Regeln an, wenn die Objekt-UUID eines Remote Prozedur Aufrufes interpretiert wird:

-   Nil-Objekt UUIDs

    Der UUID des Nil-Objekts wird automatisch der Nulltyp "uuid" zugewiesen (es ist unzulässig, eine NULL-Objekt-UUID in der [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine anzugeben). Daher wird ein Remote Prozedur aufruter, dessen Bindungs Handle ein Nil-Objekt UUID enthält, automatisch an den Manager gesendet, der mit dem Nil-Typ UUID registriert ist, sofern vorhanden.

-   Nicht-Nil-Objekt-UUIDs

    Im Prinzip sollte ein Remote Prozedur aufrucher, dessen Bindungs Handle ein nicht-Nil-Objekt UUID enthält, von einem Vorgesetzten verarbeitet werden, dessen Typ UUID mit dem Typ der UUID des Objekts übereinstimmt. Wenn Sie jedoch den richtigen Vorgesetzten identifizieren, muss der Server den Typ des Objekts "uuid" durch Aufrufen der " [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) "-Routine angegeben haben.

    Wenn ein Server die [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine für eine nicht-Nil-Objekt-UUID nicht aufrufen kann, wird ein Remote Prozedur Aufruf für das Objekt UUID an den Manager-EPV weitergeleitet, der Remote Prozedur Aufrufe mit einem Nil-Objekt UUID (d. h. der Nil-Typ UUID) aufruft.

    Remote Prozedur Aufrufe mit einer nicht-Nil-Objekt-UUID im Bindungs Handle können nicht ausgeführt werden, wenn der Server das nicht-Nil-Objekt "uuid" mit dem Typ "uuid" durch Aufrufen der [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine zugewiesen hat. es wurde jedoch nicht auch ein Manager-EPV für den Typ "uuid" registriert, indem [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)aufgerufen wurde.

In der folgenden Tabelle werden die Aktionen zusammengefasst, die von der-Lauf Zeit Bibliothek zum Auswählen der Manager-Routine verwendet werden.



| Objekt-UUID des Aufrufes | Der Servertyp für das Objekt "uuid"? | Vom Server registrierter EPV-Typ? | Dispatching-Aktion                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Trägers                 | Nicht zutreffend                   | Ja                         | Verwendet den Manager mit dem Nil-Typ UUID.                                                                                                           |
| Trägers                 | Nicht zutreffend                   | Nein                          | Fehler ( \_ \_ nicht unterstützter RPC- \_ Typ); lehnt den Remote Prozedur Aufruf ab.                                                                              |
| Nicht-NULL             | Ja                              | Ja                         | Verwendet den Manager mit dem gleichen Typ UUID.                                                                                                          |
| Nicht-NULL             | Nein                               | Wird ignoriert.                     | Verwendet den Manager mit dem Nil-Typ UUID. Wenn kein Manager mit dem Nulltyp UUID, Error (RPC \_ S \_ unsupportedtype) ist, lehnt den Remote Prozedur Aufruf ab. |
| Nicht-NULL             | Ja                              | Nein                          | Fehler (RPC \_ S \_ unsupportedtype); lehnt den Remote Prozedur Aufruf ab.                                                                                |



 

Die Objekt-UUID des Aufrufes ist das Objekt UUID, das in einem Bindungs Handle für einen Remote Prozedur Aufrufvorgang gefunden wurde.

Der Server legt den Typ der UUID des Objekts fest, indem er [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) aufruft, um den Typ UUID für ein Objekt anzugeben.

Der Server registriert den Typ für den Manager-EPV durch Aufrufen von [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) unter Verwendung desselben Typs UUID.

> [!Note]  
> Dem Nil-Objekt UUID wird immer automatisch der Nulltyp UUID zugewiesen. In der [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine ist es unzulässig, eine NULL-Objekt-UUID anzugeben.

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>Senden eines Remote Prozedur Aufrufes an eine Server-Manager-Routine

In den folgenden Tabellen sind die Schritte aufgeführt, die von der RPC-Lauf Zeit Bibliothek zum Senden eines Remote Prozedur Aufrufs an eine Server-Manager-Routine benötigt werden.

Ein einfacher Fall, bei dem der Server den Standard-Manager-EPV registriert, wird in den folgenden Tabellen beschrieben.

**Schnittstellen Registrierungs Tabelle**



| Schnittstellen-UUID | Manager-Typ UUID | Einstiegspunkt Vektor |
|----------------|-------------------|--------------------|
| *uuid1*        | Trägers               | Standard-EPV        |



 

**Objekt Registrierungs Tabelle**



| Objekt-UUID             | Objekttyp |
|-------------------------|-------------|
| Trägers                     | Trägers         |
| (Beliebige andere Objekt-UUID) | Trägers         |



 

**Mapping des Bindungs Handles zu einem Einstiegspunkt Vektor (EPV)**



| Interface UUID (aus Client Bindungs handle) | Objekt-UUID (aus Client Bindungs handle) | Objekttyp (aus Objekt Registrierungs Tabelle) | Manager-EPV (aus Schnittstellen Registrierungs Tabelle) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Trägers                                      | Trägers                                      | Standard-EPV                                 |
| Wie oben                               | *uuida*                                  | Trägers                                      | Standard-EPV                                 |



 

In den folgenden Schritten werden die Aktionen beschrieben, die die Lauf Zeit Bibliothek des RPC-Servers durchführt, wie in den vorangehenden Tabellen dargestellt, wenn ein Client mit der Schnittstelle UUID *uuid1* diese aufruft.

1.  Der Server ruft [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) auf, um eine Schnittstelle mit dem Nil-Manager-Typ UUID und dem von der Mitte generierten Standard-Manager-EPV zuzuordnen. Dieser Befehl fügt einen Eintrag in die Registrierungs Tabelle der-Schnittstelle ein. Die UUID der Schnittstelle ist in den *ifspec* -Parametern enthalten.
2.  Standardmäßig verknüpft die Objekt Registrierungs Tabelle alle Objekt-UUIDs mit dem Nil-Typ UUID. In diesem Beispiel ruft der Server " [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)" nicht auf.
3.  Die Server Lauf Zeit Bibliothek empfängt einen Remote Prozedur Code, der die Schnittstelle uuid enthält, zu der der Aufruf gehört, und das Objekt UUID aus dem Bindungs Handle des Aufrufes.

    In den folgenden Funktions Verweis Einträgen finden Sie Informationen dazu, wie ein Objekt UUID in ein Bindungs handle festgelegt wird:

    -   [**Rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**Rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**Rpcbindingsetobject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  Mithilfe der UUID-Schnittstelle aus dem Remote Prozedur Aufruf wird in der Lauf Zeit Bibliothek des Servers diese Schnittstelle uuid in der Registrierungs Tabelle der-Schnittstelle lokalisiert.

    Wenn der Server die Schnittstelle nicht mithilfe von [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)registriert hat, wird der Remote Prozedur Aufruf an den Aufrufer zurückgegeben, \_ Wenn der \_ Statuscode RPC S unbekannt ist \_ .

5.  Mithilfe der Objekt-UUID aus dem Bindungs Handle wird in der Lauf Zeit Bibliothek des Servers das Objekt UUID in der Objekt Registrierungs Tabelle angezeigt. In diesem Beispiel werden alle Objekt-UUIDs dem Nil-Objekttyp zugeordnet.
6.  Die Lauf Zeit Bibliothek des Servers gibt den Nil-Manager-Typ in der Schnittstellen Registrierungs Tabelle an.
7.  Das Kombinieren der Schnittstellen-UUID und des Nil-Typs in der Schnittstellen Registrierungs Tabelle wird in den Standard-EPV aufgelöst, der die Server-Manager-Routinen enthält, die für die im Remote Prozedur aufrufende Schnittstelle UUID ausgeführt werden sollen.

Angenommen, der Server bietet mehrere Schnittstellen und mehrere Implementierungen jeder Schnittstelle, wie in den folgenden Tabellen beschrieben.

**Schnittstellen Registrierungs Tabelle**



| Schnittstellen-UUID | Manager-Typ UUID | Einstiegspunkt Vektor |
|----------------|-------------------|--------------------|
| *uuid1*        | Trägers               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**Objekt Registrierungs Tabelle**



| Objekt-UUID      | Objekttyp |
|------------------|-------------|
| *uuida*          | *uuid3*     |
| *uuidb*          | *uuid7*     |
| *uuidc*          | *uuid7*     |
| *uuidd*          | *uuid3*     |
| *uuide*          | *uuid3*     |
| *uuidf*          | *uuid8*     |
| Trägers              | Trägers         |
| (Beliebige andere UUID) | Trägers         |



 

**Zuordnung des Bindungs Handles zu einem Einstiegspunkt Vektor**



| Interface UUID (aus Client Bindungs handle) | Objekt-UUID (aus Client Bindungs handle) | Objekttyp (aus Objekt Registrierungs Tabelle) | Manager-EPV (aus Schnittstellen Registrierungs Tabelle) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Trägers                                      | Trägers                                      | *epv1*                                      |
| *uuid1*                                     | *uuida*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidd*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuide*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidb*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidc*                                  | *uuid7*                                  | *epv3*                                      |



 

In den folgenden Schritten werden die Aktionen beschrieben, die die Lauf Zeit Bibliothek des Servers durchführt, wie in den vorangehenden Tabellen dargestellt, wenn ein Client mit der Interface UUID *uuid2* und dem Objekt UUID *uuidc* ihn aufruft.

1.  Der Server ruft [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) auf, um die angebotenen Schnittstellen den verschiedenen Manager-EPVs zuzuordnen. Die Einträge in der Schnittstellen Registrierungs Tabelle reflektieren vier Aufrufe von [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) , um zwei Schnittstellen mit zwei Implementierungen (EPVs) für jede Schnittstelle zu bieten.
2.  Der Server ruft [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) auf, um den Typ der einzelnen angebotenen Objekte festzulegen. Zusätzlich zur Standard Zuordnung des Nil-Objekts zu einem Nil-Typ werden alle anderen Objekt-UUIDs, die nicht explizit in der Objekt Registrierungs Tabelle gefunden werden, auch dem Nil-Typ UUID zugeordnet.

    In diesem Beispiel ruft der Server die [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine sechs Mal auf.

3.  Die Server Lauf Zeit Bibliothek empfängt einen Remote Prozedur Aufruf, der die Schnittstelle uuid enthält, zu der der Aufruf gehört, und eine Objekt-UUID aus dem Bindungs Handle des Aufrufes.
4.  Mithilfe der UUID-Schnittstelle aus dem Remote Prozedur Aufruf wird in der Lauf Zeit Bibliothek des Servers die Schnittstelle uuid in der Schnittstellen Registrierungs Tabelle angezeigt.
5.  Mithilfe der *uuidc* -Objekt-UUID aus dem Bindungs handle sucht die Lauf Zeit Bibliothek des Servers nach dem Objekt UUID in der Objekt Registrierungs Tabelle und ermittelt, dass es dem Typ *uuid7* zugeordnet ist.
6.  Um den Manager-Typ zu finden, kombiniert die Lauf Zeit Bibliothek des Servers die Schnittstelle UUID, *uuid2* und Type *uuid7* in der Registrierungs Tabelle der-Schnittstelle. Dies wird in *epv3* aufgelöst, das die Server-Manager-Routine enthält, die für den Remote Prozedur aufrufrufe ausgeführt werden soll.

Die Routinen in *epv2* werden nie ausgeführt, weil der Server die [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Routine nicht aufgerufen hat, um der Objekt Registrierungs Tabelle Objekte mit dem Typ "uuid" *uuid4* hinzuzufügen.

Ein Remote Prozedur Aufruf mit der Schnittstelle UUID *uuid2* und der Objekt-UUID *uuidf* kehrt an den Aufrufer mit einem unbekannten RPC- \_ \_ \_ \_ typstatus Code zurück, da der Server [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)oder [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) nicht aufgerufen hat, um die Schnittstelle mit dem Manager-Typ *uuid8* zu registrieren.

## <a name="return-values"></a>Rückgabewerte

Diese Funktion gibt einen der folgenden Werte zurück.



| Wert                             | Bedeutung                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ OK                        | Erfolg                      |
| der RPC- \_ \_ Typ ist \_ bereits \_ registriert. | Der Typ UUID ist bereits registriert. |



 

## <a name="supplying-your-own-object-inquiry-function"></a>Bereitstellen einer eigenen Object-Inquiry-Funktion

Stellen Sie sich einen Server vor, der Tausende von Objekten vieler unterschiedlicher Typen verwaltet. Wenn der Server gestartet wird, muss die Serveranwendung die [**rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) -Funktion für jedes der Objekte aufrufen, auch wenn Clients möglicherweise nur auf einige wenige Objekte verweisen (oder sich sehr viel Zeit nehmen, um darauf zu verweisen). Diese Tausenden von Objekten sind wahrscheinlich auf dem Datenträger, sodass das Abrufen ihrer Typen zeitaufwändig wäre. Außerdem dupliziert die interne Tabelle, die das Objekt UUID dem Manager-Typ "uuid" entspricht, im Wesentlichen die Zuordnung, die mit den Objekten selbst verwaltet wird.

Der Zweck der RPC-Funktion enthält die [**rpcobjectsetinqfn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn)-Funktion. Mit dieser Funktion stellen Sie Ihre eigene Objekt Abfragefunktion bereit.

Beispielsweise können Sie eine eigene Objekt Abfragefunktion bereitstellen, wenn Sie die Objekte 100 – 199 der Typnummer 1, 200 – 299 der Typnummer 2 zuordnen usw. Die Objekt Abfragefunktion kann auch auf ein verteiltes Dateisystem erweitert werden, in dem die Serveranwendung nicht über eine Liste aller verfügbaren Dateien (Objekt-UUIDs) verfügt, oder wenn Objekt-UUIDs Dateien im Dateisystem benennen und Sie nicht alle Zuordnungen zwischen Objekt-UUIDs und Typ UUIDs vorab laden möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**Rpcbindingsetobject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)
</dt> <dt>

[**Rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)
</dt> <dt>

[**Rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**Rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**Rpcobjectsettype**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**Rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**Rpcserverunregisterifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





---
title: Ändern von Schnittstellen in abwärts kompatibler Weise
description: Die in der Versions Verwaltungs Theorie für RPC und com erläuterten Methoden sind aus vielen Gründen möglicherweise nicht akzeptabel.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314daecc6b55aaf4a348411010eb578149f86921
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729801"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Ändern von Schnittstellen in abwärts kompatibler Weise

Die in [der Versions Verwaltungs Theorie für RPC und com](the-versioning-theory-for-rpc-and-com.md) erläuterten Methoden sind aus vielen Gründen möglicherweise nicht akzeptabel. Das Ändern einer Schnittstellen Version gemäß den Regeln erfordert im Wesentlichen, dass neue Clients nicht mit alten Servern kommunizieren. Dies ist bei kommerziellen Software, die im-Feld bereitgestellt wurde, oft nicht möglich. Manchmal hat Windows Schnittstellen Änderungen eingeführt, die sich auf geänderte GUIDs oder Versionen fehlen. Dies war darauf zurückzuführen, dass neue Clients mit Legacy Servern kommunizieren mussten und dass die Lösung, die ein neuer Client sowohl die alte als auch die neue Schnittstelle unterstützen würde, als unerwünscht eingestuft wurde.

## <a name="best-practice"></a>Bewährte Methode

Dies sind die angemessenen Methoden, um das Problem bei der Netzwerkverbindung zu umgehen, wenn die Schnittstellen-GUID und die Version nicht geändert werden können.

1.  Beachten Sie, dass die Anwendung die Funktionen der anderen Seite kennt.

    Der Client und der Server verfügen über ein Protokoll, mit dem jede (oder zumindest der neue Client) die Identität des Partners einrichten kann. In der Regel genügt es, dass der neue Client die von alten und neuen Servern unterstützten Funktionen kennt. Dies kann problemlos erfolgen, wenn eine Anwendung einen Verbindungs Kontext einnimmt und durch einen vom Client ausgeführten Funktionsaufruf vom Typ *xxxgetinfo* vor der Ausführung von RPC-Vorgängen unterstützt wird. Wenn eine Anwendung die Features pro Server-Freigabe verwaltet, kann ein Aufruf mit einer Inkompatibilität mit dem alten Server/Client niemals erfolgen, da die Anwendung steuert, welche Aufrufe an welchen Server ausgegeben werden. Die untere Zeile besteht darin, dass die Anwendung proaktiv verhindert, dass eine Übereinstimmung auftritt. Dies kann in Verbindung mit der zweiten Vorgehensweise erfolgen.

2.  Führen Sie eine neue Remote-API ein.

    Eine neue Remote Methode steht nicht in Konflikt mit vorhandenen Methoden, wenn Sie am Ende der-Schnittstelle hinzugefügt wird. Alte Clients können jederzeit neue Server abrufen. Der neue Client kann die neue Methode aufrufen, ohne die Identität des Servers zu kennen. Voraussetzung ist, dass die Fehler von dem aufgerufenen Server überwacht werden. Die RPC-Laufzeit prüft stets die Methoden Nummer für jede Schnittstelle vor einer Verteilung, um sicherzustellen, dass die Methode in einer geeigneten v-Tabelle liegt. Bei einer Methode, die einem Server unbekannt ist, löst die RPC-Laufzeit die Ausnahme RPC \_ S \_ procnum \_ außerhalb \_ des gültigen \_ Bereichs aus. Diese Ausnahme wird nur in dieser speziellen Situation ausgelöst. Aus diesem Grund kann ein neuer Client die Ausnahme als Vorzeichen ansehen, dass der-Befehl an einen alten Server gesendet wurde und das Verhalten ordnungsgemäß ändern kann.

3.  Führen Sie neue Parameter oder neue Datentypen nur in den neuen Methoden ein.

    Ein Grund, eine neue Methode einzuführen, besteht darin, die Daten Inkompatibilität zu vermeiden. Wenn ein neuer Datentyp eingeführt oder einfach geändert wird, sollte er grundsätzlich nur in einer neuen Methode (oder Methoden) verwendet werden. Beispiele für nicht kompatible Datentyp Änderungen finden Sie [unter Beispiele für inkompatible Änderungen](examples-of-incompatible-changes.md) . Die einzige relevante Ausnahme von dieser Regel wird in Element 4 beschrieben.

4.  Ordnen Sie neue Parameter oder neue Datentypen über einen Wrapper zu.

    Diese Lösung ist anwendbar, wenn ein neuer Parameter oder Datentyp für einen Benutzer verfügbar gemacht werden muss, aber nicht separat oder separat oder in den alten Datentypen oder-Parametern zugeordnet werden muss. Beispielsweise wird ein Remote-Befehl von vielen System-APIs umschlossen und ausgeführt. Sie werden möglicherweise eine Art von Zuordnung von den Benutzer bekannten Datentypen zu den Datentypen, die tatsächlich im zugrunde liegenden RPC-Aufruf verwendet werden, durchgeführt. Daher ist es immer sinnvoll, zu überprüfen, ob die Änderung in der Benutzeroberfläche als Änderung an eine Remote Schnittstelle weitergegeben werden muss.

    Eine ähnliche Situation kann auftreten, wenn der Benutzer eine Remote-API direkt aufruft, aber ein Wrapper eingefügt werden kann, um eine neue Typzuordnung oder andere zusätzliche Aktionen durchzuführen, die notwendig sind. Interface Definition Language (IDL) bietet mehrere Möglichkeiten, eine solche Neuzuordnung zu ermöglichen, d \[ . r. [**aufrufen \_ als**](/windows/desktop/Midl/call-as) \] , über \[ [**tragen \_ als und Übertragungs**](/windows/desktop/Midl/transmit-as) \] \[ [**\_ Mars Hall**](/windows/desktop/Midl/wire-marshal) \] . Der " \[ **\_ Callas** " \] -Attribut führt einen Funktions Wrapper auf dem Client und dem Server ein. Beide werden zwischen dem Benutzercode und dem Mars Haller platziert. Die anderen Attribute befassen sich mit der direkten Typzuordnung. Wenn Sie Erweiterungs Probleme haben, \[ **wenden Sie sich \_ so** \] an, wie es am häufigsten verwendet wird, und ist am einfachsten zu verstehen und zu bearbeiten.

5.  Ändern von Datentypen durch eine defaultless-Union.

    Das Ändern eines Attributs oder Datentyps führt in der Regel zu Netzwerk Inkompatibilität. Beispiele finden Sie [unter Beispiele für nicht kompatible Änderungen](examples-of-incompatible-changes.md) . Im Fall einer Union ohne eine DEFAULT-Klausel kann die Inkompatibilität jedoch ähnlich wie bei einer Prozedur außerhalb des gültigen Bereichs verwaltet werden, wie zuvor beschrieben. Dieses Schema kann problemlos auf die gängigen *xxxinfo* -Typen angewendet werden, die Unions verwenden.

    Beispielsweise ein solcher Beispiel

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    gibt möglicherweise Informationen auf Ebene 1, 2 oder 3 zurück, wobei *xxxinfo* eine Union mit drei Verzweigungen ist: 1, 2 und 3.

6.  Verwenden Sie das \[ [**Range**](/windows/desktop/Midl/range) - \] Attribut, um den Bereich anzugeben.

    Sie können das \[ [**Range**](/windows/desktop/Midl/range) - \] Attribut für einen einfachen Skalierungstyp ohne Unterbrechung der Abwärtskompatibilität angeben. Dieses Attribut hat keine Auswirkung auf das Wire-Format, aber während des Unmarshalling prüft RPC den Wert bei der Übertragung, um zu bestätigen, dass er innerhalb des in der IDL-Datei angegebenen Bereichs liegt. Andernfalls \_ wird eine ungültige RPC X- \_ \_ gebundene Ausnahme ausgelöst. Dies ist besonders nützlich, wenn der Server die maximale Größe eines Arrays in der Größe kennt.

    Beispiel:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

Das RPC-Verhalten, wenn die festgestellte Ebene 4 ist und der Arm fehlt, hängt von der Definition der Union ab. Bei einer Union, bei der die default-Klausel definiert ist, überträgt RPC einen Typ, der in der default-Klausel für alle anderen als die bekannten Arm-Bezeichnungen angegeben ist (in diesem Fall etwas anderes als 1, 2 oder 3). Für eine defaultless-Union löst der unmars Haller eine Ausnahme aus, da es in der Definition keinen Standardwert gibt, auf den zurückgegriffen wird. Die Ausnahme ist ein \_ Ungültiges RPC S- \_ \_ Tag.

Auch hier kann ein neuer Client sein Verhalten anpassen, wenn er feststellt, dass er als Alter Server bezeichnet wurde.

Aus diesen empfohlenen Vorgehensweisen besteht folgendes: Wenn ein Remote barer Datentyp entworfen werden muss, der in Zukunft erweitert werden kann, verwenden Sie eine defaultless-Union in der IDL-Datei. Wenn Sie eine Auswahl treffen, ist eine gekapselte Union etwas sauberer.

Aufgrund von quirllie interner Darstellung des NDR64 Wire-Protokolls muss die Empfehlung zum Hinzufügen von Waffen, die weiter oben in diesem Abschnitt bereitgestellt wurde, wie folgt qualifiziert werden: der neue Arm, der hinzugefügt wird, kann die Ausrichtung der Union nicht ändern, und insbesondere sollte die größte Ausrichtung der Waffen nicht geändert werden. Dies ist in der Regel kein Problem, da ein Zeiger in einem Arm die Ausrichtung auf 8 erzwingt. Ein Entwurf, bei dem jeder Arm ein Zeiger auf einen Arm-Typ ist, ist eine saubere Methode zum erfüllen der Anforderung.

 

 
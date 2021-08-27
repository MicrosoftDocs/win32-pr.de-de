---
title: Ändern von Schnittstellen auf abwärtskompatible Weise
description: Die in The Versioning Theory for RPC and COM (Die Versionsthematik für RPC und COM) erläuterten Methoden können aus vielen Gründen nicht akzeptabel sein.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbe06be3106b4c599baed2d625eefa1f9c7d035c70ef89ac325406bb8c2037d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022960"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Ändern von Schnittstellen auf abwärtskompatible Weise

Die in [The Versioning Theory for RPC and COM (Die Versionsthematik für RPC und COM)](the-versioning-theory-for-rpc-and-com.md) erläuterten Methoden können aus vielen Gründen nicht akzeptabel sein. Das Ändern einer Schnittstellenversion gemäß den Regeln erfordert im Wesentlichen, dass neue Clients nicht mit alten Servern kommunizieren. Dies ist bei kommerzieller Software, die vor Ort bereitgestellt wird, häufig nicht möglich. Manchmal wurden durch Windows Schnittstellenänderungen eingeführt, die nicht in geänderten GUIDs oder Versionen vorhanden sind. Dies war das Ergebnis neuer Clients, die mit Legacyservern kommunizieren mussten, und weil die Lösung, die ein neuer Client sowohl die alte als auch die neue Schnittstelle unterstützen würde, als unerwünscht betrachtet wurde.

## <a name="best-practice"></a>Bewährte Methode

Dies sind die sinnvollen Methoden zum Umgehen des Wire Incompatibility-Problems, wenn die Schnittstellen-GUID und die Version nicht geändert werden können.

1.  Achten Sie darauf, dass die Anwendung die Funktionen der anderen Seite kennt.

    Der Client und der Server verfügen über ein Protokoll, mit dem jeder (oder zumindest der neue Client) die Identität des Partners einrichten kann. In der Regel ist es ausreichend, dass der neue Client die von alten und neuen Servern unterstützten Features kennt. Dies kann problemlos erfolgen, wenn eine Anwendung an einem Verbindungskontext gebunden ist, und kann über einen vom Client ausgeführten *XxxGetInfo-Funktionsaufruftyp* unterstützt werden, bevor RPC-Vorgänge ausgeführt werden. Wenn eine Anwendung die Features pro Serverversion verwaltet, kann nie ein Aufruf mit Inkompatibilität mit dem alten Server/Client erfolgen, da die Anwendung steuert, welche Aufrufe an welchen Server ausgegeben werden. Unterm Strich verhindert die Anwendung proaktiv einen Konflikt. Dies kann in Verbindung mit der zweiten Übung erfolgen.

2.  Führen Sie eine neue Remote-API ein.

    Eine neue Remotemethode tritt nicht mit vorhandenen Methoden in Konflikt, wenn sie ganz am Ende der Schnittstelle hinzugefügt wird. Alte Clients können neue Server wie gewohnt aufrufen. Der neue Client kann die neue Methode aufrufen, ohne die Identität des Servers zu kennen, vorausgesetzt, er überwacht die Fehler, die vom aufgerufenen Server stammen. Die RPC-Laufzeit überprüft immer die Methodennummer für jede Schnittstelle vor einem Dispatch, um sicherzustellen, dass sich die Methode innerhalb einer geeigneten v-Tabelle befindet. Bei einer Methode, die einem Server unbekannt ist, löst die RPC-Laufzeit die Ausnahme RPC \_ S \_ PROCNUM \_ OUT OF RANGE \_ \_ aus. Diese Ausnahme wird nur in dieser speziellen Situation ausgelöst. Daher kann ein neuer Client auf die Ausnahme als Hinweis darauf achten, dass der Aufruf an einen alten Server gesendet wurde, und sein Verhalten ordnungsgemäß ändern.

3.  Führen Sie neue Parameter oder neue Datentypen nur in den neuen Methoden ein.

    Ein Grund für die Einführung einer neuen Methode ist die Vermeidung von Dateninkompatibilität. Wenn ein neuer Datentyp eingeführt oder einfach geändert wird, sollte er im Prinzip nur in einer neuen Methode (oder Methode) verwendet werden. Beispiele für inkompatible Datentypänderungen finden Sie unter Beispiele für inkompatible [Änderungen.](examples-of-incompatible-changes.md) Die einzige wichtige Ausnahme von dieser Regel wird in Element 4 beschrieben.

4.  Ordnen Sie neue Parameter oder neue Datentypen über einen Wrapper zu.

    Diese Lösung gilt, wenn ein neuer Parameter oder Datentyp für einen Benutzer verfügbar gemacht werden muss, aber nicht separat remote sein muss oder den alten Datentypen oder Parametern zugeordnet werden kann. Viele System-APIs drehen sich beispielsweise um und führen einen Remoteaufruf aus. Es kann sein, dass sie eine Art von Zuordnung von bekannten Datentypen des Benutzers zu den Datentypen durchführen, die tatsächlich im zugrunde liegenden RPC-Aufruf verwendet werden. Daher ist es immer sinnvoll, zu prüfen, ob die Änderung in der Benutzeroberfläche als Änderung an eine Remoteschnittstelle verbreitet werden muss.

    Eine ähnliche Situation kann auftreten, wenn der Benutzer eine Remote-API direkt aufruft, aber ein Wrapper eingeführt werden kann, um eine neue Typzuordnung oder einige andere zusätzliche Aktionen durchzuführen, die notwendig geworden sind. Die Schnittstellendefinitionssprache (Interface Definition Language, IDL) bietet mehrere Möglichkeiten, diese Neuzuordnung zu vereinfachen, nämlich \[ [**aufrufen \_ als**](/windows/desktop/Midl/call-as) \] , übertragen \[ [**\_ als**](/windows/desktop/Midl/transmit-as) \] und Kabel \[ [**\_ marshallen.**](/windows/desktop/Midl/wire-marshal) \] Der \[ **Aufruf \_ als** \] Attribut führt einen Funktionswrapper auf dem Client und Server ein. Beide werden zwischen dem Benutzercode und dem Marshaller platziert. Die anderen Attribute behandeln die direkte Typzuordnung. Rufen Sie bei Erweiterungsproblemen \[ **\_ wie** \] am häufigsten verwendet auf, und ist am einfachsten zu verstehen und ohne Fallstricke zu bearbeiten.

5.  Ändern von Datentypen über eine standardlose Union.

    Das Ändern eines Attributs oder Datentyps führt in der Regel zu einer Inkompatibilität von Kabeln. Beispiele finden Sie unter [Beispiele für inkompatible Änderungen.](examples-of-incompatible-changes.md) Im Fall einer Union ohne Standardklausel kann die Inkompatibilität jedoch ähnlich wie bei einer Prozedur außerhalb des zulässigen Bereichs verwaltet werden, wie zuvor beschrieben. Dieses Schema kann problemlos auf die beliebten *XxxINFO-Typen* angewendet werden, die Unions verwenden.

    Beispiel: Ein Aufruf wie dieser

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    kann Informationen auf Ebene 1, 2 oder 3 zurückgeben, wobei *XxxINFO* eine Union mit drei Verzweigungen ist: 1, 2 und 3.

6.  Verwenden Sie das \[ [](/windows/desktop/Midl/range) \] Bereichsattribut, um den Bereich anzugeben.

    Sie können das \[ [](/windows/desktop/Midl/range) \] Bereichsattribut für einen einfachen Skalierungstyp angeben, ohne die Abwärtskompatibilität zu beeinträchtigen. Dieses Attribut wirkt sich nicht auf das Wire-Format aus, aber während des Aufhebens der Zuordnung überprüft RPC den Wert bei der Verkabelung, um sicherzustellen, dass er innerhalb des in der IDL-Datei angegebenen Bereichs liegt. Wenn dies nicht der Fall ist, wird eine RPC \_ X \_ INVALID \_ BOUND-Ausnahme ausgelöst. Dies ist besonders nützlich, wenn der Server die maximale Größe eines Arrays mit größe kennt.

    Beispiel:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

Das RPC-Verhalten, wenn die angegebene Ebene 4 ist und der Arm fehlt, hängt von der Definition der Union ab. Bei einer Union mit der definierten Standardklausel überträgt RPC einen in der Standardklausel angegebenen Typ für alles, was sich von den bekannten Armbezeichnungen unterscheidet (in diesem Fall alles andere als 1, 2 oder 3). Bei einer standardlosen Union löst der Unmarshaler eine Ausnahme aus, da es definitionsgemäß keinen Standardwert gibt, auf den ein Fallback erfolgt. Die Ausnahme ist RPC \_ S \_ INVALID \_ TAG.

Auch hier kann ein neuer Client sein Verhalten anpassen, wenn festgestellt wird, dass er einen alten Server aufgerufen hat.

Aus diesen empfohlenen Methoden ergibt sich Folgendes: Wenn ein remotabler Datentyp entworfen werden muss, der in Zukunft erweitert werden kann, verwenden Sie eine standardlose Union in der IDL-Datei. Bei einer Auswahl ist eine gekapselte Union etwas übersichtlicher.

Aufgrund der Eigenheiten der internen Darstellung des NDR64-Wire-Protokolls muss die Empfehlung zum Hinzufügen von Armen, die weiter oben in diesem Abschnitt bereitgestellt wurden, wie folgt qualifiziert werden: Der neue Arm, der hinzugefügt wird, kann die Ausrichtung der Union nicht ändern, und insbesondere die größte Ausrichtung der Arme sollte sich nicht ändern. Dies ist in der Regel kein Problem, da ein Zeiger in einem Arm die Ausrichtung auf 8 erzwingt. Ein Entwurf, bei dem jeder Arm ein Zeiger auf einen Armtyp ist, ist eine saubere Möglichkeit, die Anforderung zu erfüllen.

 

 
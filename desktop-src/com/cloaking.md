---
title: Cloaking (com)
description: Das Cloaking ist eine com-Sicherheitsfunktion, die bestimmt, welche Identität der Client während des Identitäts Wechsels auf den Server projiziert.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588651cfa37def4e174ef0f2fdba9b79b0c60ca8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "103869316"
---
# <a name="cloaking-com"></a>Cloaking (com)

Das Cloaking ist eine com-Sicherheitsfunktion, die bestimmt, welche Identität der Client während des Identitäts Wechsels auf den Server projiziert. Wenn das Cloaking festgelegt ist, maskiert der zwischen Server seine eigene Identität und stellt die Identität des Clients für den Server dar, den er im Auftrag des Clients aufruft. Allem die Client Identität, die vom Server erkannt wird, ist die Identität, die dem Proxy zugeordnet ist. Die Identität des Proxys wird durch verschiedene Faktoren bestimmt. eine davon ist der Typ der festgelegten Art von Verstopfungen (sofern vorhanden). Das clonel wird vom SChannel-Sicherheitsanbieter nicht unterstützt.

Die folgenden Themen enthalten weitere Informationen zum Verlust:

-   [Arten von Verstopfungen](#types-of-cloaking)
-   [Auswirkungen der Cloaking auf die Client Identität](#how-cloaking-affects-client-identity)
-   [Festlegen des Cloaking](#setting-cloaking)
-   [Verstopfungen und Identitätswechsel Ebenen](#cloaking-and-impersonation-levels)
-   [Cloaking-Szenarien](#cloaking-scenarios)
-   [Zugehörige Themen](#related-topics)

## <a name="types-of-cloaking"></a>Arten von Verstopfungen

Es gibt zwei Arten von Verstopfungen: *statischer* und *dynamischer* Cloaking:

-   Bei statischem Cloaking (eoac \_ static \_ Cloaking) sieht der Server das Thread Token vom ersten-Client an den Server. Für den ersten-Befehl wird die Proxy Identität verwendet, wenn die Proxy Identität zuvor während eines Aufrufes von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)festgelegt wurde. Wenn die Proxy Identität jedoch nicht zuvor festgelegt wurde, wird das Thread Token verwendet. Wenn kein Thread Token vorhanden ist, wird das Prozess Token verwendet. Bei allen zukünftigen aufrufen wird die für den ersten Aufruf festgelegte Identität verwendet.
-   Mit dynamischem Cloaking (eoac \_ Dynamic \_ Cloaking) wird bei jedem-Rückruf das aktuelle Thread Token (wenn ein Thread Token vorhanden ist) verwendet, um die Identität des Clients zu bestimmen. Wenn kein Thread Token vorhanden ist, wird das Prozess Token verwendet. Dies bedeutet, dass bei Servern, die im Auftrag des Clients während des Identitäts Wechsels aufgerufen werden, die Identität des com-Clients angezeigt wird, von dem der Aufruf stammt, was im Allgemeinen das gewünschte Verhalten ist. (Um einen Identitätswechsel erfolgreich durchführen zu können, muss der Client die Server Autorität zum Annehmen der Identität durch Festlegen einer entsprechenden Identitätswechsel Ebene erhalten. Weitere Informationen finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md).) Diese Art des Cloaking ist aufwendig.

## <a name="how-cloaking-affects-client-identity"></a>Auswirkungen der Cloaking auf die Client Identität

Wenn ein verschlüsselter-Vorgang ausgeführt wird und der Server die Identität des Clients anfordert, wird die Identität, die an den Proxy gebunden ist, in der Regel abgerufen. (Manchmal führt der Authentifizierungsdienst eine Übersetzung von der tatsächlichen Identität aus, aber im Allgemeinen ist die Proxy Identität die Identität, die der Server sieht.) Der Proxy stellt eine Identität für den Server dar, die vom Typ der festgelegten Knoten und anderen Faktoren abhängig ist.

Zusammenfassend gilt: die Identität des Clients ist eine Funktion des festgelegten Cloaking-Flags, des Prozess Tokens, des Vorhandenseins oder Fehlens eines Thread Tokens und der Angabe, ob die Proxy Identität zuvor festgelegt wurde. In der folgenden Tabelle wird die resultierende Proxy Identität (Client Identität) angezeigt, wenn diese Faktoren variieren.



| Cloaking von Flags                     | Thread-tokenpräsenz  | Zuvor festgelegte Proxy Identität | Proxy Identität (Client Identität)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Cloaking nicht festgelegt<br/>        | Ist doch egal<br/>  | Ist doch egal<br/>         | Prozess Token oder Authentifizierungs Identität<br/> |
| statische eoac- \_ \_ Cloaking<br/>  | Anzahl<br/>     | Nein<br/>                 | Thread Token<br/>                             |
| statische eoac- \_ \_ Cloaking<br/>  | Anzahl<br/>     | Ja<br/>                | Aktuelle Proxy Identität<br/>                   |
| statische eoac- \_ \_ Cloaking<br/>  | Nicht vorhanden<br/> | Nein<br/>                 | Prozess Token<br/>                            |
| statische eoac- \_ \_ Cloaking<br/>  | Nicht vorhanden<br/> | Ja<br/>                | Aktuelle Proxy Identität<br/>                   |
| Dynamisches eoac- \_ \_ Cloaking<br/> | Anzahl<br/>     | Ist doch egal<br/>         | Thread Token<br/>                             |
| Dynamisches eoac- \_ \_ Cloaking<br/> | Nicht vorhanden<br/> | Ist doch egal <br/>        | Prozess Token<br/>                            |



 

Im folgenden Flussdiagramm wird veranschaulicht, wie die Proxy Identität in unterschiedlichen Situationen bestimmt wird.

![Diagramm, das den Ablauf zum Ermitteln der Proxy Identität anzeigt.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Festlegen des Cloaking

Das Cloaking wird als funktionsflag in einem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-aufrufswert festgelegt, der das Cloaking für den gesamten Prozess festlegt. Diese Funktion wird dann so lange festgelegt, bis der Client Sie durch einen IClientSecurity::[**setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Befehl (oder an [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)) ändert, wodurch das Cloaking für den Proxy festgelegt wird.

Standardmäßig ist das Cloaking nicht festgelegt. Um dies festzulegen, übergeben Sie \_ das statische eoac- \_ Cloaking oder das dynamische eoac- \_ \_ Cloaking an den *pfunktionalitäten* -Parameter in [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).

Wenn statischer Cloaking mithilfe von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aktiviert wird, übernimmt jeder Proxy ein Token (Thread oder Prozess), wenn Sie zum ersten Mal einen Aufruf für den Proxy durchführen. Wenn das statische Cloaking mithilfe von [**setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)aktiviert wird, übernimmt der Proxy das Token zu diesem Zeitpunkt im Thread. Wenn kein Thread Token verfügbar ist, wenn **setblanket** aufgerufen wird, wird das Prozess Token für die Identität des Proxys verwendet. Im Grunde korrigiert **setblanket** die Identität des Proxys.

Bei dynamischer Verschleierung wird die Identität des Proxys auf die gleiche Weise bestimmt, unabhängig davon, ob das dynamische Cloaking mithilfe von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder mit [**setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)festgelegt wird. Das aktuelle Thread Token wird verwendet, wenn es vorhanden ist. Andernfalls wird das Prozess Token verwendet.

Wenn für den gesamten Prozess durch einen Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ein Cloaking festgelegt wird und Sie Aufrufe mit dem Prozess Token durchführen möchten, nehmen Sie beim Aufrufen von Aufrufen keinen Identitätswechsel vor.

## <a name="cloaking-and-impersonation-levels"></a>Verstopfungen und Identitätswechsel Ebenen

Wie bereits erwähnt, wird durch die Funktion zur Verschleierung festgelegt, welche Identität einem Server während des Identitäts Wechsels angezeigt wird. Das Cloaking bietet einem Server die Möglichkeit, eine andere Identität als die eigene Identität auf einen anderen Server zu projizieren, der im Auftrag des Clients aufgerufen wird. Die Identitätswechsel Ebene gibt an, wie viel Autorität der Client dem Server zugewiesen hat.

Der Identitätswechsel ohne Verschleierung funktioniert, ist jedoch möglicherweise nicht die beste Wahl, da der endgültige Server in einigen Fällen die Identität des ursprünglichen Aufrufers kennen muss. Dies kann nicht erreicht werden, ohne dass ein Cloaking verwendet werden muss, da es schwierig ist sicherzustellen, dass nur autorisierte Clients auf einen Remote Computer zugreifen können. Wenn der Identitätswechsel ohne Verschleierung verwendet wird, ist die Identität, die einem Downstreamserver vorgelegt wird, der für den unmittelbaren aufrufenden Prozess.

Allerdings ist das Cloaking ohne Identitätswechsel nicht sinnvoll. Das Cloaking ist nur sinnvoll, wenn der Client eine Identitätswechsel Ebene von Identitätswechsel oder Delegaten festgelegt hat. (Bei niedrigeren Identitätswechsel Ebenen kann der Server keine verdeckten Aufrufe durchführen.) Ob das Cloaking erfolgreich ist, hängt von der Anzahl der überquerten Computer Grenzen und der Identitätswechsel Ebene ab, die angibt, wie viel Autorität der Server für den Client benötigt.

In einigen Situationen ist es sinnvoll, dass der Server einen Cloaking festlegt, wenn der Client die Identitätswechsel Ebene auf RPC- \_ C- \_ IMP-Stufen Identitätswechsel festlegt \_ \_ . Es gelten jedoch bestimmte Einschränkungen. Wenn der ursprüngliche Client die Identitätswechsel Ebene auf RPC- \_ C-IMP-Stufen Identitätswechsel festlegt \_ \_ \_ , kann sich der zwischen Server (der als Client auf dem gleichen Computer fungiert) nur über eine Computer Grenze verbergen. Dies liegt daran, dass ein Identitätswechsel Token auf Identitäts Ebene nur über eine Computer Grenze hinweg übermittelt werden kann. Nachdem die Computer Grenze überschritten wurde, kann nur auf lokale Ressourcen zugegriffen werden. Die Identität, die dem Server vorgelegt wird, hängt vom Typ des festgelegten Knotentyps ab. Wenn kein Cloaking festgelegt ist, ist die Identität, die einem Server vorgelegt wird, der Prozess, der den sofortigen Rückruf durchführt.

Wenn Sie über mehrere Computer Grenzen verfügen möchten, müssen Sie ein geeignetes Funktions Kennzeichen und einen Identitätswechsel auf delegatebene angeben. Bei dieser Art von Identitätswechsel werden dem Server sowohl die lokalen Anmelde Informationen als auch die Netzwerk Anmelde Informationen des Clients zugewiesen, sodass das Identitätswechsel Token beliebig viele Computer Grenzen überschreiten kann. Auch hier ist die Identität, die dem Server vorgelegt wird, abhängig vom Typ der festgelegten Art von Verstopfungen. Wenn kein Cloaking mit Identitätswechsel auf delegatebene festgelegt wird, ist die Identität, die einem Server vorgelegt wird, der der aufrufenden Prozess.

Nehmen wir beispielsweise an, "Process A" ruft "b" auf, und b ruft "C. b" auf Wenn sich A, B und c auf demselben Computer befinden, funktioniert das Übergeben des Identitätswechsel Tokens von a an B und dann an c. Wenn sich A und C auf demselben Computer befinden und b nicht ist, wird das Übergeben des Tokens zwischen A und b, jedoch nicht von b zu C ausgeführt. Der-Befehl von b zu C schlägt fehl, weil B C beim Durchführen eines clolovers nicht aufgerufen werden kann. Wenn jedoch die Identitätswechsel Ebene auf Delegat festgelegt wird, kann das Token von B an C und der Aufruf erfolgreich ausgeführt werden.

## <a name="cloaking-scenarios"></a>Cloaking-Szenarien

In der folgenden Abbildung wird von Process A der Aufruf B aufgerufen, C wird aufgerufen, D wird aufgerufen, wenn das Cloaking nicht festgelegt ist. Folglich sieht jeder zwischen Prozess die Identität des Prozesses, der ihn aufgerufen hat.

![Diagramm, das den Prozess anzeigt, wenn das Cloaking nicht festgelegt ist.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Bei statischem Cloaking sieht der Server die Proxy Identität, die während des ersten Aufrufes vom Client an den Server festgelegt wurde. Die folgende Abbildung zeigt ein Beispiel für die Proxy Identität, die während eines Aufrufes von B an C festgelegt wird. Bei einem nachfolgenden-Vorgang wird von Prozess D die Identität von b erkannt, wenn das statische Cloaking durch b und C festgelegt wird.

![Diagramm, das den Prozess für den statischen Cloaking anzeigt.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Bei dynamischem Cloaking basiert die Identität des Aufrufers während des Identitäts Wechsels auf dem aktuellen Thread Token (sofern vorhanden). Die folgende Abbildung zeigt die Situation, in der b und C dynamische Cloaking festlegen und D die Identität eines anzeigt, trotz eines früheren Aufrufes von b zu c.

![Diagramm, das den Prozess für dynamisches Cloaking anzeigt.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> </dl>

 


---
title: Cloaking (COM)
description: Die Verleumdung ist eine COM-Sicherheitsfunktion, die bestimmt, welche Identität der Client während des Identitätswechsels auf den Server projiziert.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5d36ec4561b0cc3290f21f4c46dc338b6df455bc694464812f2274b8c1345f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462980"
---
# <a name="cloaking-com"></a>Cloaking (COM)

Die Verleumdung ist eine COM-Sicherheitsfunktion, die bestimmt, welche Identität der Client während des Identitätswechsels auf den Server projiziert. Wenn die Verdeckung festgelegt ist, maskiert der Zwischenserver seine eigene Identität und stellt die Identität des Clients dem Server vor, den er im Auftrag des Clients aufruft. Im Grunde genommen: Die Clientidentität, die vom Server erkannt wird, ist die Identität, die dem Proxy zugeordnet ist. Die Identität des Proxys wird durch mehrere Faktoren bestimmt, von denen einer der Typ der Verleumdung ist, der festgelegt wird (falls vorhanden). Die Verdeckung wird vom Schannel-Sicherheitsanbieter nicht unterstützt.

Die folgenden Themen enthalten weitere Informationen zum Verschluss:

-   [Typen der Verleumdung](#types-of-cloaking)
-   [Auswirkungen der Verleumdung auf die Clientidentität](#how-cloaking-affects-client-identity)
-   [Festlegen der Verleumdung](#setting-cloaking)
-   [Verleumdungs- und Identitätswechselebenen](#cloaking-and-impersonation-levels)
-   [Verleumdungsszenarien](#cloaking-scenarios)
-   [Zugehörige Themen](#related-topics)

## <a name="types-of-cloaking"></a>Typen der Verleumdung

Es gibt zwei Arten der Verleumdung: *statisches* Und *dynamisches* Verleumden:

-   Mit statischem Cloaking (EOAC \_ STATIC \_ CLOAKING) sieht der Server das Threadtoken vom ersten Aufruf eines Clients an den Server. Beim ersten Aufruf wird diese Proxyidentität verwendet, wenn die Proxyidentität zuvor während eines Aufrufs von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)festgelegt wurde. Wenn die Proxyidentität zuvor jedoch nicht festgelegt wurde, wird das Threadtoken verwendet. Wenn kein Threadtoken vorhanden ist, wird das Prozesstoken verwendet. Für alle zukünftigen Aufrufe wird die identität verwendet, die beim ersten Aufruf festgelegt wurde.
-   Beim dynamischen Cloaking (EOAC \_ DYNAMIC \_ CLOAKING) wird bei jedem Aufruf das aktuelle Threadtoken (wenn ein Threadtoken vorhanden ist) verwendet, um die Identität des Clients zu bestimmen. Wenn kein Threadtoken vorhanden ist, wird das Prozesstoken verwendet. Dies bedeutet, dass Server, die während des Identitätswechsels im Namen des Clients aufgerufen werden, die Identität des COM-Clients sehen, der den Aufruf ausgelöst hat. Dies ist im Allgemeinen das gewünschte Verhalten. (Damit der Identitätswechsel erfolgreich ist, muss der Client die Serverautorität zum Identitätswechsel erteilt haben, indem eine geeignete Identitätswechselebene festgelegt wird. Weitere Informationen finden Sie unter [Identitätswechselebenen](impersonation-levels.md).) Diese Art der Verleumdung ist teuer.

## <a name="how-cloaking-affects-client-identity"></a>Auswirkungen der Verleumdung auf die Clientidentität

Wenn ein verschlüsselter Aufruf erfolgt und der Server den Client nach seiner Identität fragt, erhält er in der Regel die Identität, die an den Proxy gebunden ist. (Manchmal führt der Authentifizierungsdienst eine Übersetzung aus der tatsächlichen Identität durch, aber im Allgemeinen ist die Proxyidentität die Identität, die der Server sieht.) Der Proxy stellt dem Server eine Identität bereit, die vom Typ der festgelegten Verleumdung und anderen Faktoren abhängt.

Zusammenfassend lässt sich feststellen, dass die Identität des Clients eine Funktion des festgelegten Verleumdungsflags, des Prozesstokens, des Vorhandenseins oder Fehlens eines Threadtokens und der Angabe ist, ob die Proxyidentität zuvor festgelegt wurde. Die folgende Tabelle zeigt die resultierende Proxyidentität (Clientidentität), wenn diese Faktoren variieren.



| Verleumderungsflags                     | Vorhandensein von Threadtoken  | Proxyidentität, die zuvor festgelegt wurde | Proxyidentität (Clientidentität)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Cloaking not set<br/>        | Ist doch egal<br/>  | Ist doch egal<br/>         | Prozesstoken oder Authentifizierungsidentität<br/> |
| \_STATISCHES \_ EOAC-CLOAKING<br/>  | Anzahl<br/>     | Nein<br/>                 | Threadtoken<br/>                             |
| \_STATISCHES \_ EOAC-CLOAKING<br/>  | Anzahl<br/>     | Ja<br/>                | Aktuelle Proxyidentität<br/>                   |
| \_STATISCHES \_ EOAC-CLOAKING<br/>  | Nicht vorhanden<br/> | Nein<br/>                 | Prozesstoken<br/>                            |
| \_STATISCHES \_ EOAC-CLOAKING<br/>  | Nicht vorhanden<br/> | Ja<br/>                | Aktuelle Proxyidentität<br/>                   |
| \_DYNAMISCHE \_ EOAC-CLOAKING<br/> | Anzahl<br/>     | Ist doch egal<br/>         | Threadtoken<br/>                             |
| \_DYNAMISCHE \_ EOAC-CLOAKING<br/> | Nicht vorhanden<br/> | Ist doch egal <br/>        | Prozesstoken<br/>                            |



 

Das folgende Flussdiagramm veranschaulicht, wie die Proxyidentität in verschiedenen Situationen bestimmt wird.

![Diagramm, das den Ablauf zum Bestimmen der Proxyidentität zeigt.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Festlegen der Verleumdung

Cloaking wird als Funktionsflag in einem Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)festgelegt, das die Verleumdung für den gesamten Prozess festlegt. Die Verleumdungsfunktion wird dann festgelegt, bis der Client sie durch einen Aufruf von IClientSecurity::[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (oder [**coSetProxyBlanket)**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)ändert, wodurch die Verleumdung für den Proxy festgelegt wird.

Standardmäßig ist die Verleumdung nicht festgelegt. Um sie festzulegen, übergeben Sie EOAC \_ STATIC \_ CLOAKING oder EOAC \_ DYNAMIC \_ CLOAKING an den *pCapabilities-Parameter* in [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**SetBlanket.**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)

Wenn statisches Cloaking mit [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aktiviert ist, ruft jeder Proxy beim ersten Aufruf des Proxys ein Token (Thread oder Prozess) ab. Wenn statisches Cloaking mit [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)aktiviert ist, nimmt der Proxy das Token zu diesem Zeitpunkt im Thread ab. Wenn beim Aufruf von **SetBlanket** kein Threadtoken verfügbar ist, wird das Prozesstoken für die Identität des Proxys verwendet. Im Grunde behebt **SetBlanket** die Identität des Proxys.

Bei der dynamischen Verleumdung wird die Identität des Proxys auf die gleiche Weise bestimmt, unabhängig davon, ob die dynamische Verleumdung mit [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder mit [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)festgelegt wird. Das aktuelle Threadtoken wird verwendet, wenn eins vorhanden ist. Andernfalls wird das Prozesstoken verwendet.

Wenn die Verleumdung für den gesamten Prozess durch einen Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) festgelegt ist und Sie Aufrufe mit dem Prozesstoken durchführen möchten, nehmen Sie während der Aufrufe keine Identität an.

## <a name="cloaking-and-impersonation-levels"></a>Verleumdungs- und Identitätswechselebenen

Wie bereits erwähnt, bestimmt die Verleumdungsfunktion, welche Identität einem Server während des Identitätswechsels präsentiert wird. Die Verleumdung bietet einem Server die Möglichkeit, eine andere Identität als die eigene auf einen anderen Server zu pro projectieren, den er im Auftrag des Clients aufruft. Die Identitätswechselebene gibt an, wie viel Autorität der Client dem Server erteilt hat.

Der Identitätswechsel ohne Verleumdung funktioniert, aber es ist möglicherweise nicht die beste Wahl, da der endgültige Server in einigen Fällen die Identität des ursprünglichen Aufrufers kennen muss. Dies kann nicht ohne Verleumdung erreicht werden, da es schwierig ist, sicherzustellen, dass nur autorisierte Clients auf einen Remotecomputer zugreifen können. Wenn der Identitätswechsel ohne Verleumdung verwendet wird, entspricht die Identität, die einem Downstreamserver angezeigt wird, dem unmittelbar aufrufenden Prozess.

Das Verleumden ist jedoch ohne Identitätswechsel nicht sinnvoll. Eine Verleumdung ist nur sinnvoll, wenn der Client die Identitätswechselebene "Identitätswechsel" oder "Delegat" festgelegt hat. (Bei niedrigeren Identitätswechselebenen kann der Server keine verleumderten Aufrufe vornehmen.) Ob die Verleumdung erfolgreich ist, hängt von der Anzahl der überschrittenen Computergrenzen und von der Identitätswechselebene ab. Dies gibt an, wie groß die Autorität ist, die der Server im Auftrag des Clients agieren muss.

In einigen Situationen ist es sinnvoll, dass der Server das Verdecken festlegt, wenn der Client die Identitätswechselebene auf RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE festlegt. Es gelten jedoch bestimmte Einschränkungen. Wenn der ursprüngliche Client die Identitätswechselebene auf RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE festlegt, kann der Zwischenserver (der als Client auf demselben Computer fungiert) nur über eine Computergrenze hinweg verdecken. Dies liegt daran, dass ein Identitätswechseltoken auf Identitätswechselebene nur über eine Computergrenze übergeben werden kann. Nachdem die Computergrenze überschritten wurde, kann nur auf lokale Ressourcen zugegriffen werden. Die identität, die dem Server angezeigt wird, hängt von der Art der Verleumdung ab, die festgelegt ist. Wenn keine Verleumdung festgelegt ist, entspricht die Identität, die einem Server angezeigt wird, der Identität des Prozesses, der den sofortigen Aufruf vornimmt.

Um mehrere Computergrenzen zu verleumdern, müssen Sie sowohl ein geeignetes Verleumdungsfunktionsflag als auch einen Identitätswechsel auf Delegatebene angeben. Bei diesem Identitätswechseltyp werden dem Server sowohl die lokalen anmeldeinformationen als auch die Netzwerkanmeldeinformationen des Clients übergeben, sodass das Identitätswechseltoken eine beliebige Anzahl von Computergrenzen überschreiten kann. Auch hier hängt die identität, die dem Server angezeigt wird, von der Art der Verleumdung ab, die festgelegt ist. Wenn kein Cloaking mit Identitätswechsel auf Delegatebene festgelegt ist, entspricht die identität, die einem Server angezeigt wird, der des Prozesses, der den Aufruf vornimmt.

Angenommen, Prozess A ruft B auf, und B ruft C auf. B hat die Verleumdung festgelegt, und A hat die Identitätswechselebene für den Identitätswechsel festgelegt. Wenn sich A, B und C auf demselben Computer befinden, funktioniert die Übergabe des Identitätswechseltokens von A an B und dann an C. Wenn sich A und C jedoch auf demselben Computer befinden und B nicht ist, funktioniert die Übergabe des Tokens zwischen A und B, aber nicht von B nach C. Der Aufruf von B zu C schlägt fehl, da B C während der Verleumdung nicht aufrufen kann. Wenn A jedoch die Identitätswechselebene als Delegat festlegt, kann das Token von B an C übergeben werden, und der Aufruf kann erfolgreich sein.

## <a name="cloaking-scenarios"></a>Verleumdungsszenarien

In der folgenden Abbildung ruft Prozess A B auf, ruft C auf, ruft D auf, wenn die Verleumdung nicht festgelegt ist. Daher sieht jeder Zwischenprozess die Identität des Prozesses, der ihn aufgerufen hat.

![Diagramm, das den Prozess zeigt, wenn die Verleumdung nicht festgelegt ist.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Mit statischem Cloaking sieht der Server die Proxyidentität, die während des ersten Aufrufs vom Client an den Server festgelegt wurde. Die folgende Abbildung zeigt ein Beispiel für die Proxyidentität, die während eines Aufrufs von B zu C festgelegt wird. Bei einem nachfolgenden Aufruf erkennt Prozess D die Identität von B, wenn die statische Verleumdung von B und C festgelegt wird.

![Diagramm, das den Prozess der statischen Verleumdung zeigt.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Bei der dynamischen Verleumdung basiert die Identität des Aufrufers während des Identitätswechsels auf dem aktuellen Threadtoken, sofern vorhanden. Die folgende Abbildung zeigt die Situation, in der B und C die dynamische Verleumdung festlegen und D die Identität von A trotz eines früheren Aufrufs von B nach C sieht.

![Diagramm, das den Prozess für die dynamische Verleumdung zeigt.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> </dl>

 


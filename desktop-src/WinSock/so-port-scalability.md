---
description: Aktiviert die Skalierbarkeit lokaler Ports für einen Socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 925d6337bc5b9d4633117fc1d8e1b8db2657f31b91a9cce602702ceb67e7e92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993370"
---
# <a name="so_port_scalability"></a>ALSO \_ \_ PORTSKALIERBARKEIT

Die **Option SO PORT \_ \_ SCALABILITY** socket ermöglicht die Skalierbarkeit lokaler Ports für einen Socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**ALSO \_ \_ PORTSKALIERBARKEIT**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



Die **Option SO PORT \_ \_ SCALABILITY** socket ermöglicht die Skalierbarkeit lokaler Ports, da die Portzuordnung maximiert werden kann, indem Platzhalterports für verschiedene lokale Adressportpaare auf einem lokalen Computer mehrmals zugewiesen werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Hinweis: Verwenden Sie auf Plattformen, auf denen sowohl SO \_ PORT \_ SCALABILITY als auch SO \_ REUSE \_ UNICASTPORT unterstützt werden, die Verwendung von SO \_ REUSE \_ UNICASTPORT.

Proxyserverumgebungen weisen aufgrund der eingeschränkten lokalen Portverfügbarkeit Skalierbarkeitsprobleme auf. Eine Möglichkeit, dies zu umgehen, besteht darin, dem Computer weitere IP-Adressen hinzuzufügen. Platzhalterports, die mit der [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) verwendet werden, sind jedoch standardmäßig auf die Größe des dynamischen Portbereichs auf dem lokalen Computer beschränkt (bis zu 64.000 Ports, aber in der Regel weniger), unabhängig von der Anzahl der IP-Adressen auf dem lokalen Computer. Um dies zu umgehen, muss die Anwendung ihren eigenen Portpool entweder mit Portreservierung oder mit Heuristik verwalten.

Um zu vermeiden, dass jede Anwendung, die Skalierbarkeit erfordert, ihren eigenen Portpool verwaltet und eine höhere Skalierbarkeit bei gleichzeitiger Aufrechterhaltung der Anwendungskompatibilität ermöglicht, hat Windows Server 2008 die Option **SO \_ PORT \_ SCALABILITY** Socket eingeführt, um die Platzhalterportzuordnung zu maximieren. Die Portzuordnung wird maximiert, indem eine Anwendung Platzhalterports für jedes eindeutige lokale Adress- und Portpaar zuordnen kann. Wenn ein lokaler Computer also über vier IP-Adressen verfügt, können bis zu 256.000 Platzhalterports (64.000 Ports × 4 IP-Adressen) durch [**Platzhalterbindungsfunktionen**](/windows/desktop/api/winsock/nf-winsock-bind) zugewiesen werden.

Wenn die **OPTION SO \_ PORT \_ SCALABILITY** socket für einen Socket festgelegt ist und ein Aufruf der [**Bindungsfunktion**](/windows/desktop/api/winsock/nf-winsock-bind) für eine angegebene Adresse und einen Platzhalterport erfolgt (der *Name-Parameter* wird mit einer bestimmten Adresse und einem Port 0 festgelegt), ordnet Winsock einen Port für die angegebene Adresse zu. Diese Zuordnung basiert auf allen möglichen IP-Adressen und Ports/pro Adresse auf dem lokalen Computer. Wenn ein Platzhalterport mithilfe der OPTION **SO \_ PORT \_ SCALABILITY** bezogen wird, kann dieser Port nicht von einem anderen Socket ohne die OPTION **SO PORT \_ \_ SCALABILITY** zugeordnet werden. Diese Einschränkung ist vorhanden, um Abwärtskompatibilitätsprobleme mit Anwendungen zu vermeiden, die davon ausgehen, dass ein lokaler Platzhalterport nicht wiederverwendet werden kann. Beachten Sie, dass dies bedeutet, dass Anwendungen, die mithilfe von **SO \_ PORT \_ SCALABILITY** eine große Anzahl von Ports abrufen, ältere Anwendungen von Ports verhungern können. Wenn alle verfügbaren kurzlebigen Ports für mindestens eine Adresse mit **SO \_ PORT \_ SCALABILITY** abgerufen wurden, sind ohne die Socketoption keine weiteren Platzhalterportzuordnungen möglich.

Um Auswirkungen zu haben, muss die OPTION **SO \_ PORT \_ SCALABILITY** festgelegt werden, bevor die [**Bindungsfunktion**](/windows/desktop/api/winsock/nf-winsock-bind) aufgerufen wird. Ein Beispiel dafür, wie dies auf einem Computer mit zwei Adressen verwendet wird, wird unten beschrieben:

-   Die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) wird von einem Prozess zum Erstellen eines Sockets aufgerufen.
-   Die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) wird aufgerufen, um die **OPTION SO PORT \_ \_ SCALABILITY** Socket für den neu erstellten Socket zu aktivieren.
-   Die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) wird aufgerufen, um eine Bindung an eine der IP-Adressen und Port 0 des lokalen Computers zu übertragen.
-   Die [**Connect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) wird dann aufgerufen, um eine Verbindung mit einer Remote-IP-Adresse herzustellen. Der Socket wird von der Anwendung nach Bedarf verwendet.
-   Eine [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) wird vom gleichen Prozess (möglicherweise einem anderen Thread) aufgerufen, um einen zweiten Socket zu erstellen.
-   Die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) wird aufgerufen, um die OPTION **SO PORT \_ \_ SCALABILITY** Socket für den neu erstellten zweiten Socket zu aktivieren.
-   Die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) wird mit der zweiten IP-Adresse des lokalen Computers und Port 0 aufgerufen. Selbst wenn alle Ports zuvor zugeordnet wurden, ist dieser Aufruf erfolgreich, da auf dem lokalen Computer mehrere IP-Adressen verfügbar sind und die **OPTION SO \_ PORT \_ SCALABILITY** Socket für beide Sockets im selben Prozess festgelegt wurde.
-   Die [**Connect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) wird dann aufgerufen, um eine Verbindung mit einer Remote-IP-Adresse herzustellen. Der zweite Socket wird von der Anwendung nach Bedarf verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Ws2def.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**SOL SOCKET Socket Options (SOL \_ SOCKET-Socketoptionen)**](sol-socket-socket-options.md)
</dt> <dt>

[**Socketoptionen**](socket-options.md)
</dt> </dl>

 

 





---
description: Aktiviert die Skalierbarkeit des lokalen Ports für einen Socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129120"
---
# <a name="so_port_scalability"></a>\_Port \_ Skalierbarkeit

Die **Option \_ Port \_ Skalierbarkeits** Socket ermöglicht die lokale Port Skalierbarkeit für einen Socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_Port \_ Skalierbarkeit**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



Die **Option \_ Port \_ Skalierbarkeits** -Socket ermöglicht die lokale Port Skalierbarkeit, indem die Zuordnung von Port Belegungen für unterschiedliche lokale Adress Port Paare auf einem lokalen Computer mehrfach zugelassen wird.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Hinweis: auf Plattformen, auf denen sowohl \_ \_ die Port Skalierbarkeit als auch \_ die Wiederverwendung von \_ unicastport unterstützt werden, bevorzugen Sie die Verwendung von " \_ \_ unicastport".

Proxy Serverumgebungen haben aufgrund eingeschränkter lokaler Port Verfügbarkeit Skalierbarkeits Probleme. Eine Möglichkeit, dieses Problem zu umgehen, besteht darin, dem Computer weitere IP-Adressen hinzuzufügen. Standardmäßig sind für die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion verwendete Platzhalter Anschlüsse jedoch auf die Größe des dynamischen Port Bereichs auf dem lokalen Computer beschränkt (bis zu 64K Ports, aber in der Regel weniger), unabhängig von der Anzahl der IP-Adressen auf dem lokalen Computer. Um dies zu umgehen, muss die Anwendung ihren eigenen Port Pool entweder mit Port Reservierung oder mithilfe von Heuristik verwalten.

Um zu vermeiden, dass jede Anwendung, die Skalierbarkeit erfordert, einen eigenen Port Pool verwaltet und eine größere Skalierbarkeit ermöglicht, während die Anwendungs Kompatibilität gewahrt bleibt, wurde mit Windows Server 2008 die Socketoption " **\_ Port \_ Skalierbarkeit** " eingeführt, um die Platz Zuweisung von Platzhaltern zu maximieren Die Port Zuordnung wird maximiert, indem es einer Anwendung ermöglicht, Platzhalter Anschlüsse für jede eindeutige lokale Adresse und jedes einzelne Port Paar zuzuordnen. Wenn ein lokaler Computer also über vier IP-Adressen verfügt, können bis zu 256 k Platzhalter Anschlüsse (64 K-Ports × 4 IP-Adressen) durch Platzhalter [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Funktionsanforderungen zugeordnet werden.

Wenn die **Option \_ Port \_ Skalierbarkeits** -Socket für einen Socket festgelegt ist und ein Aufrufen der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion für eine angegebene Adresse und einen Platzhalter Anschluss erfolgt (der *Name* -Parameter wird mit einer bestimmten Adresse und dem Port 0 festgelegt), wird von Winsock ein Port für die angegebene Adresse zugeteilt. Diese Zuordnung basiert auf allen möglichen IP-Adressen und Ports/pro Adresse auf dem lokalen Computer. Wenn ein Platzhalter Anschluss mithilfe der Option **" \_ Port \_ Skalierbarkeit** " abgerufen wird, kann dieser Port nicht von einem anderen Socket zugeordnet werden, ohne dass die Option " **\_ Port \_ Skalierbarkeit** " verwendet wird. Diese Einschränkung ist vorhanden, um Probleme mit der Abwärtskompatibilität bei Anwendungen zu vermeiden, die davon ausgehen, dass ein Platzhalter lokaler Port nicht wieder verwendet werden kann. Dies bedeutet, dass Anwendungen, die eine große Anzahl von Ports mithilfe der **\_ Port \_ Skalierbarkeit** abrufen, ältere Anwendungen von Ports verhungern können. Wenn alle verfügbaren kurzlebigen Ports für mindestens eine Adresse mit der **\_ Port \_ Skalierbarkeit** abgerufen wurden, sind keine weiteren Platzhalter Port Zuordnungen ohne die Socketoption möglich.

Um einen Effekt zu haben, muss die Option **\_ Port \_ Skalierbarkeit** festgelegt werden, bevor die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion aufgerufen wird. Ein Beispiel dafür, wie dies auf einem Computer mit zwei Adressen verwendet wird, ist im folgenden aufgeführt:

-   Die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion wird von einem Prozess aufgerufen, um einen Socket zu erstellen.
-   Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion wird aufgerufen, um die Option " **\_ Port \_ Skalierbarkeit** " für den neu erstellten Socket zu aktivieren.
-   Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion wird aufgerufen, um eine Bindung für eine der IP-Adressen des lokalen Computers und Port 0 durchzuführen.
-   Die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion wird dann aufgerufen, um eine Verbindung mit einer Remote-IP-Adresse herzustellen. Der Socket wird von der Anwendung nach Bedarf verwendet.
-   Eine [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) wird vom gleichen Prozess (möglicherweise einem anderen Thread) aufgerufen, um einen zweiten Socket zu erstellen.
-   Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion wird aufgerufen, um die Option " **\_ Port \_ Skalierbarkeits** -Socket" für den neu erstellten zweiten Socket zu aktivieren.
-   Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion wird mit der zweiten IP-Adresse des lokalen Computers und Port 0 aufgerufen. Auch wenn alle Ports zuvor zugeordnet wurden, ist dieser Vorgang erfolgreich, da auf dem lokalen Computer mehrere IP-Adressen verfügbar sind und die Option **\_ Port \_ Skalierbarkeits** -Socket für beide Sockets im gleichen Prozess festgelegt wurde.
-   Die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion wird dann aufgerufen, um eine Verbindung mit einer Remote-IP-Adresse herzustellen. Der zweite Socket wird von der Anwendung nach Bedarf verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Ws2def. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Optionen des Sol- \_ socketsockets**](sol-socket-socket-options.md)
</dt> <dt>

[**Socketoptionen**](socket-options.md)
</dt> </dl>

 

 





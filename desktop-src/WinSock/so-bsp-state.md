---
description: Gibt die lokale Adresse, den lokalen Port, die Remote Adresse, den Remoteport, den Sockettyp und das von einem Socket verwendete Protokoll zurück.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: SO_BSP_STATE Socket-Option (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755057"
---
# <a name="so_bsp_state-socket-option"></a>Die \_ Option "BSP \_ State Socket"

Die Option " **so \_ BSP \_ State** Socket" gibt die lokale Adresse, den lokalen Port, die Remote Adresse, den Remoteport, den Sockettyp und das von einem Socket verwendete Protokoll zurück.

Um diesen Vorgang auszuführen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion mit den folgenden Parametern aufrufen.

## <a name="socket-option-value"></a>Wert der Socketoption

Die Konstante, die diese Socketoption darstellt, ist 0x1009.

## <a name="syntax"></a>Syntax


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Ein Deskriptor, der den Socket identifiziert.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Ebene, auf der die Option definiert ist. Verwenden Sie für diesen Vorgang den **Sol- \_ Socket** .

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Die Socketoption, für die der Wert abgerufen werden soll. Verwenden Sie für diesen Vorgang **also den \_ BSP- \_ Zustand** .

</dd> <dt>

*optval* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Puffer, in dem der Wert für die angeforderte Option zurückgegeben werden soll. Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur ist.

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Größe des *optval* -Puffers in Bytes. Diese Größe muss größer oder gleich der Größe einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) NULL zurück.

Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Das Netzwerk Subsystem ist fehlgeschlagen.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur.<br/> |
| <dl> <dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                                                            |
| <dl> <dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Der *Level* -Parameter ist unbekannt oder ungültig.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der " **so \_ BSP \_ State** Socket"-Option aufgerufen wird, ruft die lokale Adresse, den lokalen Port, die Remote Adresse, den Remoteport, den Sockettyp und das Protokoll ab, die von Die Option " **so \_ BSP \_ State** Socket" funktioniert mit IPv6-oder IPv4-Sockets (der " **AF \_ inet6** " und " **AF \_ inet** Address Families").

Wenn die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion erfolgreich ist, werden die Informationen in einer [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstruktur im Puffer zurückgegeben, auf den der *optval* -Parameter zeigt. Die Ganzzahl, auf die *optlen* zeigt, sollte ursprünglich die Größe dieses Puffers enthalten. bei der Rückgabe wird die Länge des Werts, der im *optval* -Parameter zurückgegeben wird, auf die Länge in Bytes festgelegt.

Die Member **isockettype** und **iProtocol** in der zurückgegebenen [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur werden für den socketdeskriptor im *s* -Parameter ausgefüllt.

Wenn sich der Socket in einem verbundenen oder gebundenen Zustand befindet, wird der **localaddr** -Member der zurückgegebenen [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur auf eine [sockaddr](sockaddr-2.md) -Struktur festgelegt, die die lokale Adresse und den Port darstellt. Wenn sich der Socket in einem verbundenen Zustand befindet, wird der **remoteaddr** -Member der zurückgegebenen **csaddr- \_ Informations** Struktur auf eine sockaddr-Struktur festgelegt, die die Remote Adresse und den Port darstellt.

Wenn sich der Socket nicht in einem verbundenen oder gebundenen Zustand befindet, wird der **localaddr** -Member der zurückgegebenen [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur mit einem **null** -Zeiger im **lpsockaddr** -Member und dem **isockaddrlength** -Element auf 0 (null) zurückgegeben. Wenn sich der Socket nicht in einem gebundenen Zustand befindet, wird der **remoteaddr** -Member der zurückgegebenen **csaddr- \_ Informations** Struktur mit einem **null** -Zeiger im **lpsockaddr** -Member und dem **isockaddrlength** -Element auf 0 (null) zurückgegeben.

Wenn die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion ausfällt, bleiben die *optval* -und *optlen* -Parameter unverändert, und der *optval* -Parameter verweist nicht auf eine zurückgegebene [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur.

Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Ws2def. h (Include Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**csaddr- \_ Informationen**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 

---
description: Gibt die lokale Adresse, den lokalen Port, die Remoteadresse, den Remoteport, den Sockettyp und das Protokoll zurück, die von einem Socket verwendet werden.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: SO_BSP_STATE Socketoption (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff165eaef1f773f41c93f1c9905588b8d715f64e89ea0cbf06d53eb656bc91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111250"
---
# <a name="so_bsp_state-socket-option"></a>SO \_ BSP \_ STATE-Socketoption

Die **Option SO \_ BSP \_ STATE** socket gibt die lokale Adresse, den lokalen Port, die Remoteadresse, den Remoteport, den Sockettyp und das Protokoll zurück, die von einem Socket verwendet werden.

Rufen Sie zum Ausführen dieses Vorgangs die [**getsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockopt) mit den folgenden Parametern auf.

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

*-Ebene* \[ In\]
</dt> <dd>

Die Ebene, auf der die Option definiert ist. Verwenden Sie **SOL \_ SOCKET** für diesen Vorgang.

</dd> <dt>

*optname* \[ In\]
</dt> <dd>

Die Socketoption, für die der Wert abgerufen werden soll. Verwenden Sie **SO \_ BSP \_ STATE** für diesen Vorgang.

</dd> <dt>

*optval* \[ out\]
</dt> <dd>

Ein Zeiger auf den Puffer, in dem der Wert für die angeforderte Option zurückgegeben werden soll. Dieser Parameter sollte auf einen Puffer zeigen, der gleich oder größer als die Größe einer [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) ist.

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Größe des *optval-Puffers* in Bytes. Diese Größe muss gleich oder größer als die Größe einer [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 0 (null) zurück.

Wenn der Vorgang fehlschlägt, wird der Wert SOCKET \_ ERROR zurückgegeben, und ein bestimmter Fehlercode kann durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Vor der Verwendung dieser Funktion muss ein erfolgreicher [**WSAStartup-Aufruf**](/windows/desktop/api/winsock/nf-winsock-wsastartup) erfolgen.<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Fehler beim Netzwerksubsystem.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *optval-* oder *optlen-Parameter* verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzeradressraums befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen-Parameter* zeigt, kleiner als die Größe einer [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) ist.<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockierende Windows Sockets 1.1-Aufruf wird ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Der *level-Parameter* ist unbekannt oder ungültig.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebenen Protokollfamilie nicht unterstützt.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die [**getockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) die mit der **Socketoption SO \_ BSP \_ STATE** aufgerufen wird, ruft die lokale Adresse, den lokalen Port, die Remoteadresse, den Remoteport, den Sockettyp und das Protokoll ab, die von einem Socket verwendet werden. Die **So \_ BSP \_ STATE-Socketoption** funktioniert mit IPv6- oder IPv4-Sockets (die AF **\_ INET6-** und **AF INET-Adressfamilien). \_**

Wenn die [**getsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockopt) erfolgreich ist, werden die Informationen in einer [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) im Puffer zurückgegeben, auf den der *optval-Parameter* zeigt. Die ganze Zahl, auf die *optlen* zeigt, sollte ursprünglich die Größe dieses Puffers enthalten. Bei der Rückgabe wird sie auf die Länge des werts in Bytes festgelegt, der im *optval-Parameter* zurückgegeben wird.

Die **Member iSocketType** und **iProtocol** in der zurückgegebenen [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) werden für den Socketdeskriptor im *s-Parameter* ausgefüllt.

Wenn sich der Socket in einem verbundenen oder gebundenen Zustand befindet, wird der **LocalAddr-Member** der zurückgegebenen [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) auf eine [SOCKADDR-Struktur](sockaddr-2.md) festgelegt, die die lokale Adresse und den Port darstellt. Wenn sich der Socket in einem verbundenen Zustand befindet, wird der **RemoteAddr-Member** der zurückgegebenen **CSADDR \_ INFO-Struktur** auf eine SOCKADDR-Struktur festgelegt, die die Remoteadresse und den Port darstellt.

Wenn sich der Socket nicht in einem verbundenen oder gebundenen Zustand befindet, wird der **LocalAddr-Member** der zurückgegebenen [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) mit einem **NULL-Zeiger** im **lpSockaddr-Member** und dem **iSockaddrLength-Member** auf 0 (null) zurückgegeben. Wenn sich der Socket nicht in einem gebundenen Zustand befindet, wird der **RemoteAddr-Member** der zurückgegebenen **CSADDR \_ INFO-Struktur** mit einem **NULL-Zeiger** im **lpSockaddr-Member** und dem **iSockaddrLength-Member** auf 0 (null) zurückgegeben.

Wenn die [**getsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockopt) fehlschlägt, bleiben die *Parameter optval* und *optlen* unverändert, und der *optval-Parameter* verweist nicht auf eine [**zurückgegebene CSADDR \_ INFO-Struktur.**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)

Beachten Sie, dass die *Headerdatei Ws2def.h* automatisch in *Winsock2.h* enthalten ist und niemals direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Ws2def.h (einschließlich Winsock2.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 

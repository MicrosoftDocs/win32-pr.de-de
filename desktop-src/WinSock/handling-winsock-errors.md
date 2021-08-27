---
description: Fehlerbehandlung in Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Behandeln von Winsock-Fehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbb0ea47fc023ce0d6ae47f82a6bb9d732e052d5749fe58f9a405d6784d941b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097900"
---
# <a name="handling-winsock-errors"></a>Behandeln von Winsock-Fehlern

Die Windows Sockets 2-Funktionen geben nicht die spezifische Ursache eines Fehlers zurück, wenn die Funktion zurückgegeben wird. Einige Winsock-Funktionen geben bei Erfolg den Wert 0 zurück. Andernfalls wird der Wert SOCKET ERROR (-1) zurückgegeben, und eine bestimmte Fehlernummer kann durch Aufrufen der \_ [**WSAGetLastError-Funktion abgerufen**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) werden. Für Winsock-Funktionen, die ein Handle zurückgeben, gibt der Rückgabewert INVALID SOCKET (0xffff) einen Fehler an, und eine bestimmte Fehlernummer kann durch Aufrufen von \_ **WSAGetLastError abgerufen werden.** Für Winsock-Funktionen, die einen Zeiger zurückgeben, gibt der Rückgabewert **NULL** einen Fehler an, und eine bestimmte Fehlernummer kann durch Aufrufen der **WSAGetLastError-Funktion abgerufen** werden.

Ein Winsock-Fehlercode kann zur Verwendung in einem Remoteprozeduraufruf (RPC) mithilfe von HRESULT FROM WIN32 in ein HRESULT \_ \_ konvertiert werden. In früheren Versionen des Platform Software Development Kit (SDK) wurde HRESULT \_ FROM \_ WIN32 in der *Headerdatei "Winerror.h"* als Makro definiert. Im Microsoft Windows Software Development Kit (SDK) wird HRESULT \_ FROM \_ WIN32 als Inlinefunktion in der *Winerror.h-Headerdatei* definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Socketfehlercodes](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 




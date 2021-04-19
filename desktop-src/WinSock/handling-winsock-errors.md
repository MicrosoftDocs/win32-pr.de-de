---
description: Fehlerbehandlung in Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Behandeln von Winsock-Fehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345718"
---
# <a name="handling-winsock-errors"></a>Behandeln von Winsock-Fehlern

Die meisten Windows Sockets 2-Funktionen geben nicht die genaue Ursache eines Fehlers zurück, wenn die Funktion zurückgibt. Einige Winsock-Funktionen geben bei Erfolg den Wert 0 (null) zurück. Andernfalls wird der Wert Socket \_ -Fehler (-1) zurückgegeben, und eine bestimmte Fehlernummer kann durch Aufrufen der [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion abgerufen werden. Bei Winsock-Funktionen, die ein Handle zurückgeben, weist der Rückgabewert "Ungültiger \_ Socket (0xFFFF)" auf einen Fehler hin, und eine bestimmte Fehlernummer kann durch Aufrufen von " **WSAGetLastError**" abgerufen werden. Bei Winsock-Funktionen, die einen Zeiger zurückgeben, weist der Rückgabewert **null** auf einen Fehler hin, und eine bestimmte Fehlernummer kann durch Aufrufen der **WSAGetLastError** -Funktion abgerufen werden.

Ein Winsock-Fehlercode kann in ein HRESULT konvertiert werden, um ihn in einem Remote Prozedur Aufruf (RPC) mithilfe \_ von HRESULT aus Win32 zu verwenden \_ . In früheren Versionen des Platform Software Development Kit (SDK) war HRESULT \_ von \_ Win32 als Makro in der Header Datei " *Winerror. h* " definiert. Im Microsoft Windows Software Development Kit (SDK) wird HRESULT \_ aus \_ Win32 als Inline Funktion in der Header Datei " *Winerror. h* " definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Sockets-Fehler Codes](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 




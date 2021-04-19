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
# <a name="handling-winsock-errors"></a><span data-ttu-id="12a97-103">Behandeln von Winsock-Fehlern</span><span class="sxs-lookup"><span data-stu-id="12a97-103">Handling Winsock Errors</span></span>

<span data-ttu-id="12a97-104">Die meisten Windows Sockets 2-Funktionen geben nicht die genaue Ursache eines Fehlers zurück, wenn die Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="12a97-104">Most Windows Sockets 2 functions do not return the specific cause of an error when the function returns.</span></span> <span data-ttu-id="12a97-105">Einige Winsock-Funktionen geben bei Erfolg den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="12a97-105">Some Winsock functions return a value of zero if successful.</span></span> <span data-ttu-id="12a97-106">Andernfalls wird der Wert Socket \_ -Fehler (-1) zurückgegeben, und eine bestimmte Fehlernummer kann durch Aufrufen der [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12a97-106">Otherwise, the value SOCKET\_ERROR (-1) is returned and a specific error number can be retrieved by calling the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function.</span></span> <span data-ttu-id="12a97-107">Bei Winsock-Funktionen, die ein Handle zurückgeben, weist der Rückgabewert "Ungültiger \_ Socket (0xFFFF)" auf einen Fehler hin, und eine bestimmte Fehlernummer kann durch Aufrufen von " **WSAGetLastError**" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12a97-107">For Winsock functions that return a handle, a return value of INVALID\_SOCKET (0xffff) indicates an error and a specific error number can be retrieved by calling **WSAGetLastError**.</span></span> <span data-ttu-id="12a97-108">Bei Winsock-Funktionen, die einen Zeiger zurückgeben, weist der Rückgabewert **null** auf einen Fehler hin, und eine bestimmte Fehlernummer kann durch Aufrufen der **WSAGetLastError** -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12a97-108">For Winsock functions that return a pointer, a return value of **NULL** indicates an error and a specific error number can be retrieved by calling the **WSAGetLastError** function.</span></span>

<span data-ttu-id="12a97-109">Ein Winsock-Fehlercode kann in ein HRESULT konvertiert werden, um ihn in einem Remote Prozedur Aufruf (RPC) mithilfe \_ von HRESULT aus Win32 zu verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="12a97-109">A Winsock error code can be converted to an HRESULT for use in a remote procedure call (RPC) using HRESULT\_FROM\_WIN32.</span></span> <span data-ttu-id="12a97-110">In früheren Versionen des Platform Software Development Kit (SDK) war HRESULT \_ von \_ Win32 als Makro in der Header Datei " *Winerror. h* " definiert.</span><span class="sxs-lookup"><span data-stu-id="12a97-110">In earlier versions of the Platform Software Development Kit (SDK), HRESULT\_FROM\_WIN32 was defined as a macro in the *Winerror.h* header file.</span></span> <span data-ttu-id="12a97-111">Im Microsoft Windows Software Development Kit (SDK) wird HRESULT \_ aus \_ Win32 als Inline Funktion in der Header Datei " *Winerror. h* " definiert.</span><span class="sxs-lookup"><span data-stu-id="12a97-111">In the Microsoft Windows Software Development Kit (SDK), HRESULT\_FROM\_WIN32 is defined as an inline function in the *Winerror.h* header file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12a97-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12a97-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a97-113">Windows Sockets-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="12a97-113">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 




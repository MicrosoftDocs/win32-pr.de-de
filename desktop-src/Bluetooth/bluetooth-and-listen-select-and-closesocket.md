---
title: Bluetooth und lauschen, SELECT und closesocket
description: Bluetooth verwendet die Funktionen "lauschen", "Select" und "closesocket" ohne Änderungen der standardmäßigen Windows-Socketprogrammierung.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- closesocket
- warten
- select
- Bluetooth und lauschen
- Bluetooth und lauschen, wählen Sie
- Bluetooth und lauschen, SELECT und closesocket
- warten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473501"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="d5646-111">Bluetooth und lauschen, SELECT und closesocket</span><span class="sxs-lookup"><span data-stu-id="d5646-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="d5646-112">Bluetooth verwendet die Funktionen " [**lauschen**](/windows/desktop/api/winsock2/nf-winsock2-listen)", " [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)" und " [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) " ohne Änderungen der standardmäßigen Windows-Socketprogrammierung.</span><span class="sxs-lookup"><span data-stu-id="d5646-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="d5646-113">Wie bei Windows Sockets gibt die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion die dem Socket zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="d5646-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="d5646-114">Beim Aufrufen der Funktion " [**lauschen**](/windows/desktop/api/winsock2/nf-winsock2-listen) " wird dringend empfohlen, einen niedrigen Wert für den *Rückstands* Parameter (in der Regel 2 bis 4) zu verwenden, da nur wenige Clientverbindungen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="d5646-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="d5646-115">Dadurch werden die Systemressourcen verringert, die für die Verwendung durch den Abhör Socket reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="d5646-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5646-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5646-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5646-117">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="d5646-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="d5646-118">**closesocket**</span><span class="sxs-lookup"><span data-stu-id="d5646-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="d5646-119">**hin**</span><span class="sxs-lookup"><span data-stu-id="d5646-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="d5646-120">**Auswahl**</span><span class="sxs-lookup"><span data-stu-id="d5646-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 
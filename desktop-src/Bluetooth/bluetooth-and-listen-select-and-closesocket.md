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
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth und lauschen, SELECT und closesocket

Bluetooth verwendet die Funktionen " [**lauschen**](/windows/desktop/api/winsock2/nf-winsock2-listen)", " [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)" und " [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) " ohne Änderungen der standardmäßigen Windows-Socketprogrammierung.

Wie bei Windows Sockets gibt die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion die dem Socket zugeordneten Ressourcen frei.

Beim Aufrufen der Funktion " [**lauschen**](/windows/desktop/api/winsock2/nf-winsock2-listen) " wird dringend empfohlen, einen niedrigen Wert für den *Rückstands* Parameter (in der Regel 2 bis 4) zu verwenden, da nur wenige Clientverbindungen akzeptiert werden. Dadurch werden die Systemressourcen verringert, die für die Verwendung durch den Abhör Socket reserviert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**hin**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**Auswahl**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 
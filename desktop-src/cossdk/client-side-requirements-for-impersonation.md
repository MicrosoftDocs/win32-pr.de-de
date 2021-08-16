---
description: Client-Side Anforderungen für Identitätswechsel
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side Anforderungen für Identitätswechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb47c2ffb5f3b8e443d2dc50add83a39b5dfc1ee31a6909c34b0170a85db11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308529"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side Anforderungen für Identitätswechsel

Die folgenden beiden Einstellungen können relativ zum Identitätswechsel auf clientseitiger Seite angegeben werden:

-   Identitätswechselebene, die angibt, dass der Client versucht, die Identität des Servers zu verwenden.
-   Eine Einstellung im Active Directory-Dienst, über die das Clientkonto als "Konto ist vertraulich und kann nicht delegiert werden" markiert werden kann, wodurch die Delegierung deaktiviert wird.

Die Identitätswechselebene kann auf verschiedene Weise festgelegt werden. Wenn der Client keine Identitätswechselebene angibt, wird der computerweite Standardwert von COM verwendet. Die computerweite Standardeinstellung kann entweder mit dem Verwaltungstool "Komponentendienste" oder Dcomcnfg.exe festgelegt werden. Der Client kann auch eine bevorzugte Identitätswechselebene mit Dcomcnfg.exe angeben.

Der Client kann die Identitätswechselebene programmgesteuert angeben, indem er entweder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)– entspricht [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), das so oft wie nötig aufgerufen werden kann – oder [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)verwendet, das einmal pro Prozess aufgerufen werden kann.

Wenn der Client einen Identitätswechsel auf Delegatebene angibt – die umfassendste Autorität, die er dem Server erteilen kann –, sollte der Client unter einer Identität ausgeführt werden, die im Active Directory-Dienst ordnungsgemäß konfiguriert ist, damit seine Identität delegiert werden kann.

Ausführlichere Informationen zu Identitätswechselebenen und den Anforderungen, die für die Delegierung erfüllt sein müssen, finden Sie unter [Delegierung und Identitätswechsel.](/windows/desktop/com/delegation-and-impersonation)

COM+-Anwendungen können natürlich immer als Clients fungieren. Wenn die COM+-Anwendung eine andere Anwendung oder Ressource aufruft, wird eine Identitätswechselebene ausgedrückt. Für COM+-Serveranwendungen können Sie eine Identitätswechselebene administrativ festlegen. COM+-Bibliotheksanwendungen können keine eigene Identitätswechselebene festlegen. sie verwenden stattdessen die des Hostprozesses. Informationen zum Festlegen des Identitätswechsels für eine COM+-Anwendung finden Sie unter [Festlegen einer Identitätswechselebene.](setting-an-impersonation-level.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientidentitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> <dt>

[Serverseitige Anforderungen für Identitätswechsel](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 

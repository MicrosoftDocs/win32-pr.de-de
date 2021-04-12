---
description: Client-Side Anforderungen für den Identitätswechsel
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side Anforderungen für den Identitätswechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342409"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side Anforderungen für den Identitätswechsel

Die folgenden beiden Einstellungen können relativ zum Identitätswechsel auf der Clientseite angegeben werden:

-   Die Identitätswechsel Ebene, die angibt, dass der Client die Identität des Servers verwenden soll.
-   Eine Einstellung im Active Directory Dienst, über die das Client Konto als "Konto ist vertraulich und nicht delegiert werden" gekennzeichnet werden kann, wodurch die Delegierung deaktiviert wird.

Die Identitätswechsel Ebene kann auf verschiedene Weise festgelegt werden. Wenn der Client keine Identitätswechsel Ebene angibt, wird der Computer weite Standard von com verwendet. Der Computer weite Standard kann entweder mithilfe des Verwaltungs Programms Komponenten Dienste oder Dcomcnfg.exe festgelegt werden. Der Client kann auch eine bevorzugte Identitätswechsel Ebene mit Dcomcnfg.exe angeben.

Der Client kann die Identitätswechsel Ebene Programm gesteuert angeben. dabei wird entweder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)– Äquivalent zu [**IClientSecurity:: setblanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket)verwendet, das so oft wie erforderlich aufgerufen werden kann – oder [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), das einmal pro Prozess aufgerufen werden kann.

Wenn der Client einen Identitätswechsel auf delegatebene anzeigt – die breiteste Stelle, die er dem Server gewähren kann – muss der Client unter einer Identität ausgeführt werden, die im Active Directory-Dienst ordnungsgemäß konfiguriert ist, damit die Identität delegiert werden kann.

Weitere Details zu Identitätswechsel Ebenen und den Anforderungen für die Delegierung finden Sie unter [Delegierung und](/windows/desktop/com/delegation-and-impersonation)Identitätswechsel.

Com+-Anwendungen können natürlich immer als Clients fungieren. Wenn die COM+-Anwendung eine andere Anwendung oder Ressource aufruft, wird eine Identitätswechsel Ebene ausgedrückt. Für com+-Server Anwendungen können Sie eine Ebene für den Identitätswechsel administrativ festlegen. COM+-Bibliotheksanwendungen können Ihre eigene Identitätswechsel Ebene nicht festlegen. Sie verwenden stattdessen die des Host Prozesses. Informationen zum Festlegen des Identitäts Wechsels für eine COM+-Anwendung finden Sie unter [Festlegen einer](setting-an-impersonation-level.md)Identitätswechsel Ebene.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> <dt>

[Server seitige Anforderungen für Identitätswechsel](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 

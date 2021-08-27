---
description: Server-Side für Identitätswechsel
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side für Identitätswechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e43016428f2ff083fc5a783d05c3c79e241dcf299f3af9ca226cb4f6a2cf1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096800"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side für Identitätswechsel

Der Server führt den Identitätswechsel programmgesteuert aus. Es wird explizit davon ausgegangen, dass die Sicherheitsanmeldeinformationen des Clients mithilfe von [**CoImpersonateClient verwendet werden.**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient) Wenn der Client dem Server ausreichende Autorität erteilt hat, hat dies den Effekt, dass die Sicherheitsanmeldeinformationen des Clients durch das Serverthreadtoken und nicht durch das Prozesstoken substituiert werden.

Wenn dies geschehen ist, kann der Server beispielsweise das Clienttoken verwenden, um auf Ressourcen zu zugreifen, die mit einem Sicherheitsdeskriptor geschützt werden. Sie kann auch Aufrufe unter der Clientidentität tätigen, wenn die Verkleinerung aktiviert ist.

Der Server kann die Cloaking programmgesteuert explizit festlegen, oder er kann sich auf eine administrative Einstellung verlassen. Standardmäßig sind COM+-Anwendungen für die Verwendung der dynamischen Verkleinerung konfiguriert. Weitere Informationen finden Sie unter [Cloaking](cloaking.md).

Wenn der Server die Delegierung im Namen des Clients –mithilfe der Clientidentität über das Netzwerk – einlässt, muss die Serverprozessidentität im Active Directory-Dienst als "Vertrauenswürdig für Delegierung" gekennzeichnet werden. Andernfalls ist bei der Delegierung ein Fehler zu sehen.

Wenn die Clientidentität nicht mehr verwendet wird, kann der Server mithilfe von CoRevertToSelf auf sein eigenes [**Prozesstoken zurückverwenden.**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

Weitere Informationen zum Implementieren von Identitätswechsel und Delegierung finden Sie unter [Delegierung und Identitätswechsel.](/windows/desktop/com/delegation-and-impersonation)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client-Identitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Clientseitige Anforderungen für Identitätswechsel](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

 

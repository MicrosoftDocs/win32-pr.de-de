---
title: Server-Side Sicherheit
description: Server-Side Sicherheit
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949151"
---
# <a name="server-side-security"></a>Server-Side Sicherheit

Der Server kann mithilfe der Methoden von [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity)Sicherheitsinformationen über einen Aufrufer abrufen oder die Identität des Aufrufers annehmen. Eine Implementierung von **IServerSecurity** wird von com für das Kontext Objekt für den aktuellen-Befehl bereitgestellt, wenn Standard-Marshalling verwendet wird. Diese Schnittstelle ist jedoch möglicherweise nicht für einige benutzerdefinierte gemarshallte Schnittstellen vorhanden.

Wenn ein Anruf beim Server eingeht, kann der Server [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) aufrufen, um einen Zeiger auf die [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) -Schnittstelle zu erhalten. Mit diesem Zeiger können die **IServerSecurity** -Methoden vom Server aufgerufen werden, um herauszufinden, was die Authentifizierungs Einstellungen des Clients sind, und um bei Bedarf die Identität des Clients anzunehmen. Das **IServerSecurity** -Objekt ist in jedem Thread im Apartment gültig, bis der von **IServerSecurity** dargestellte Befehl abgeschlossen ist. Weitere Informationen zum Identitätswechsel finden Sie unter Identitätswechsel [und-Verschleierung](impersonation.md) [.](cloaking.md)

Die folgenden Hilfsfunktionen, die auf der [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) -Schnittstellen Implementierung des callkontextobjekts basieren, sind ebenfalls verfügbar:

-   [**Coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**Coreverttself**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 
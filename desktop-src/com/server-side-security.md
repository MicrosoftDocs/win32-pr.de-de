---
title: Server-Side Sicherheit
description: Server-Side Sicherheit
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7349b318361cfd27969817ec6be9d16accacd29dce625f572a51a7b3bc8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611010"
---
# <a name="server-side-security"></a>Server-Side Sicherheit

Der Server kann Mithilfe der Methoden von [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity)Sicherheitsinformationen zu einem Aufrufer abrufen oder die Identität des Aufrufers angenommen haben. Eine Implementierung von **IServerSecurity** wird von COM für das Kontextobjekt für den aktuellen Aufruf bereitgestellt, wenn standardmäßiges Marshalling verwendet wird. Diese Schnittstelle kann jedoch für einige benutzerdefinierte Marshallingschnittstellen fehlen.

Wenn ein Aufruf beim Server eintrifft, kann der Server [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) aufrufen, um einen Zeiger auf die [**IServerSecurity-Schnittstelle zu**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) erhalten. Mit diesem Zeiger können **IServerSecurity-Methoden** vom Server aufgerufen werden, um herauszufinden, was die Authentifizierungseinstellungen des Clients sind, und um bei Bedarf die Identität des Clients zu imitieren. Das **IServerSecurity-Objekt** ist für jeden Thread im Apartment gültig, bis der durch **IServerSecurity** dargestellte Aufruf abgeschlossen ist. Weitere Informationen zum Identitätswechsel finden Sie unter [Identitätswechsel](impersonation.md) und [Verkleinern von](cloaking.md).

Die folgenden Hilfsfunktionen, die auf der [**IServerSecurity-Schnittstellenimplementierung**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) des Aufrufkontextobjekts basieren, sind ebenfalls verfügbar:

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 
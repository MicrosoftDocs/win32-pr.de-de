---
title: Identitätswechselebenen (COM)
description: Wenn der Identitätswechsel erfolgreich ist, bedeutet dies, dass der Client zugestimmt hat, den Server zu einem gewissen Grad als Client zuzulassen.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca691c89e7ff4a12e279ae0ecd0fd04cb31a951c8ac3f2671201fe99dd5900a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756390"
---
# <a name="impersonation-levels"></a>Identitätswechselebenen

Wenn der Identitätswechsel erfolgreich ist, bedeutet dies, dass der Client zugestimmt hat, den Server zu einem gewissen Grad als Client zuzulassen. Die unterschiedlichen Identitätswechselgrade werden als *Identitätswechselebenen* bezeichnet und geben an, wie viel Autorität dem Server erteilt wird, wenn er die Identität des Clients angibt.

Derzeit gibt es vier Identitätswechselebenen: *anonym,* *identifizieren,* *identitätieren* und *delegieren.* In der folgenden Liste werden die einzelnen Identitätswechselebenen kurz beschrieben:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS)
</dt> <dd>

Der Client ist gegenüber dem Server anonym. Der Serverprozess kann den Client imitieren, das Identitätswechseltoken enthält jedoch keine Informationen über den Client. Diese Ebene wird nur über den lokalen prozessübergreifenden Kommunikationstransport unterstützt. Alle anderen Transporte stufen diese Ebene automatisch zur Identifizierung herauf.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY)
</dt> <dd>

Die Standardebene des Systems. Der Server kann die Identität des Clients abrufen und den Client imitieren, um ACL-Überprüfungen auszuführen.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE)
</dt> <dd>

Der Server kann als der Client auftreten und dabei dessen Sicherheitskontext imitieren. Der Server kann als Client auf lokale Ressourcen zugreifen. Wenn der Server lokal ist, kann er als Client auf Netzwerkressourcen zugreifen. Wenn der Server remote ist, kann er nur auf Ressourcen zugreifen, die sich auf demselben Computer wie der Server befinden.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegat (RPC \_ C \_ IMP \_ LEVEL \_ DELEGATE)
</dt> <dd>

Die umfassendste Ebene des Identitätswechsels. Wenn diese Ebene ausgewählt wird, kann der Server (sowohl lokal als auch remote) als Client auftreten und dabei dessen Sicherheitskontext imitieren. Während des Identitätswechsels können die Anmeldeinformationen des Clients (sowohl lokal als auch netzwerkseitig) an eine beliebige Anzahl von Computern übergeben werden.

Damit der Identitätswechsel auf Delegatebene funktioniert, müssen die folgenden Anforderungen erfüllt sein:

-   Der Client muss die Identitätswechselebene auf RPC \_ C \_ IMP \_ LEVEL DELEGATE \_ festlegen.
-   Das Clientkonto darf im Active Directory-Dienst nicht als "Konto ist vertraulich und kann nicht delegiert werden" gekennzeichnet werden.
-   Das Serverkonto muss im Active Directory-Dienst mit dem Attribut "Vertrauenswürdig für delegierung" gekennzeichnet werden.
-   Die Computer, auf denen der Client, der Server und alle "Downstreamserver" gehostet werden, müssen alle in einer Domäne ausgeführt werden.

</dd> </dl>

Durch Auswählen der Identitätswechselebene teilt der Client dem Server mit, wie weit er beim Identitätswechsel des Clients gehen kann. Der Client legt die Identitätswechselebene auf dem Proxy fest, den er für die Kommunikation mit dem Server verwendet.

## <a name="setting-the-impersonation-level"></a>Festlegen der Identitätswechselebene

Es gibt zwei Möglichkeiten, die Identitätswechselebene festzulegen:

-   Der Client kann ihn über einen Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)prozessweit festlegen.
-   Ein Client kann die Sicherheit auf Proxyebene für eine Schnittstelle eines Remoteobjekts über einen Aufruf von [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (oder der Hilfsfunktion [**CoSetProxyBlanket)**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)festlegen.

Sie legen die Identitätswechselebene fest, indem Sie einen entsprechenden RPC \_ C \_ IMP \_ LEVEL \_ xxx-Wert über den *dwImpLevel-Parameter* an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) übergeben.

Verschiedene Authentifizierungsdienste unterstützen den Identitätswechsel auf Delegatebene in unterschiedlichen Ausmaßen. NTLMSSP unterstützt beispielsweise thread- und prozessübergreifenden Identitätswechsel auf Delegatebene, jedoch nicht computerübergreifend. Andererseits unterstützt das Kerberos-Protokoll Identitätswechsel auf Delegatebene über Computergrenzen hinweg, während Schannel keinen Identitätswechsel auf Delegatebene unterstützt. Wenn Sie über einen Proxy auf Identitätswechselebene verfügen und die Identitätswechselebene auf Delegate festlegen möchten, sollten Sie [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) mithilfe der Standardkonstanten für jeden Parameter außer der Identitätswechselebene aufrufen. COM wählt NTLM lokal und das Kerberos-Protokoll remote aus (wenn das Kerberos-Protokoll funktioniert).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> </dl>

 

 
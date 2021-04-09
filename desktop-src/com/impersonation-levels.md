---
title: Identitätswechsel Ebenen (com)
description: Wenn der Identitätswechsel erfolgreich ist, bedeutet dies, dass der Client zugestimmt hat, den Server zu einem gewissen Grad zu machen.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858483"
---
# <a name="impersonation-levels"></a>Identitätswechsel Ebenen

Wenn der Identitätswechsel erfolgreich ist, bedeutet dies, dass der Client zugestimmt hat, den Server zu einem gewissen Grad zu machen. Die unterschiedlichen Stufen des Identitäts Wechsels werden als Identitätswechsel *Ebenen* bezeichnet und geben an, wie viel Autorität dem Server zugewiesen wird, wenn die Identität des Clients angenommen wird.

Derzeit gibt es vier Identitätswechsel Ebenen: *Anonym*, *identifiziert* *, annehmen* und *delegieren*. In der folgenden Liste werden die einzelnen Identitätswechsel Ebenen kurz beschrieben:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Anonym (RPC- \_ C- \_ IMP- \_ Ebene \_ Anonym)
</dt> <dd>

Der Client ist gegenüber dem Server anonym. Der Serverprozess kann den Client imitieren, das Identitätswechseltoken enthält jedoch keine Informationen über den Client. Diese Ebene wird nur über den lokalen Kommunikationsprozess für die prozessübergreifende Kommunikation unterstützt. Alle anderen Transporte Stufen diese Ebene im Hintergrund herauf, um Sie zu identifizieren.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identifizieren (RPC \_ C \_ IMP- \_ Ebene \_ identifizieren)
</dt> <dd>

Die Standardebene des Systems. Der Server kann die Identität des Clients abrufen und den Client imitieren, um ACL-Überprüfungen auszuführen.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Identität annehmen (RPC- \_ C- \_ IMP-Ebene Identität annehmen \_ \_ )
</dt> <dd>

Der Server kann als der Client auftreten und dabei dessen Sicherheitskontext imitieren. Der Server kann als Client auf lokale Ressourcen zugreifen. Wenn der Server lokal ist, kann er auf Netzwerkressourcen als Client zugreifen. Wenn der Server Remote ist, kann er nur auf Ressourcen zugreifen, die sich auf demselben Computer wie der Server befinden.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegat (RPC \_ C \_ IMP-Ebene-Delegat \_ \_ )
</dt> <dd>

Die umfassendste Ebene des Identitätswechsels. Wenn diese Ebene ausgewählt wird, kann der Server (sowohl lokal als auch remote) als Client auftreten und dabei dessen Sicherheitskontext imitieren. Während des Identitäts Wechsels können die Anmelde Informationen des Clients (sowohl lokal als auch Netzwerk) an eine beliebige Anzahl von Computern übermittelt werden.

Damit der Identitätswechsel auf der delegatebene funktioniert, müssen die folgenden Anforderungen erfüllt sein:

-   Der Client muss die Identitätswechsel Ebene auf den RPC- \_ C- \_ IMP-Ebenen-Delegaten festlegen \_ \_ .
-   Das Client Konto darf nicht als "Konto ist vertraulich und kann nicht delegiert werden" im Active Directory-Dienst gekennzeichnet sein.
-   Das Server Konto muss mit dem Attribut "Trusted for Delegation" im Active Directory-Dienst gekennzeichnet werden.
-   Die Computer, auf denen der-Client, der-Server und alle Downstream-Server gehostet werden, müssen in einer Domäne ausgeführt werden.

</dd> </dl>

Durch Auswählen der Identitätswechsel Ebene teilt der Client dem Server mit, wie weit die Identität des Clients angenommen werden kann. Der Client legt die Identitätswechsel Ebene auf dem Proxy fest, der für die Kommunikation mit dem Server verwendet wird.

## <a name="setting-the-impersonation-level"></a>Festlegen der Identitätswechsel Ebene

Es gibt zwei Möglichkeiten, die Identitätswechsel Ebene festzulegen:

-   Der Client kann ihn Processwide durch einen [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf festlegen.
-   Ein Client kann die Sicherheit auf Proxy Ebene für eine Schnittstelle eines Remote Objekts über einen [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Befehl (oder die Hilfsfunktion [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)) festlegen.

Sie legen die Identitätswechsel Ebene fest, indem Sie einen geeigneten RPC- \_ C- \_ IMP- \_ Level \_ xxx-Wert an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) über den *dwimplevel* -Parameter übergeben.

Verschiedene Authentifizierungsdienste unterstützen Identitätswechsel auf delegatebene an verschiedene Blöcke. Beispielsweise unterstützt NTLMSSP Thread übergreifende und prozessübergreifende delegatebenenidentitäts-Identitätswechsel, aber nicht Computer übergreifend. Auf der anderen Seite unterstützt das Kerberos-Protokoll Identitätswechsel auf delegatebene über Computer Grenzen hinweg, während SChannel keinen Identitätswechsel auf der delegatebene unterstützt. Wenn Sie über einen Proxy mit Identitätswechsel verfügen und die Identitätswechsel Ebene auf Delegieren festlegen möchten, sollten Sie [**setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) mithilfe der Standard Konstanten für jeden Parameter Außer der Identitätswechsel Ebene aufrufen. COM wählt NTLM lokal und das Kerberos-Protokoll Remote aus (wenn das Kerberos-Protokoll funktioniert).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung und Identitätswechsel](delegation-and-impersonation.md)
</dt> </dl>

 

 
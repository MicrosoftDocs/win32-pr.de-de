---
title: Objektmodellhierarchie
description: Die Objekte im SDO-Objektmodell sind in einer Hierarchie angeordnet. Dies bedeutet, dass Objekte in SDO Zugriff auf andere Objekte in SDO bieten.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f63b5692571bab49580251d6ef879adde8ae9a57af4c541404aabc48538e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063340"
---
# <a name="object-model-hierarchy"></a>Objektmodellhierarchie

Die Objekte im SDO-Objektmodell sind in einer Hierarchie angeordnet. Dies bedeutet, dass Objekte in SDO Zugriff auf andere Objekte in SDO bieten.

Objekte bieten auf zwei Arten Zugriff auf andere Objekte. Eine Möglichkeit besteht darin, dass das Objekt eine Schnittstelle verfügbar macht, die Methoden zum Abrufen anderer Objekte bereitstellt. Ein Beispiel für diesen Ansatz ist das Machine-Objekt. Das Machine-Objekt macht die [**ISdoMachine-Schnittstelle**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) verfügbar. Die [**ISdoMachine::GetServiceSDO-Methode**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ruft ein Service-Objekt ab. Die [**ISdoMachine::GetUserSDO-Methode**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) ruft ein Benutzerobjekt ab.

![Machine Object Exposing isdomachine interface (Isdomachine-Schnittstelle verfügbar machendes Computerobjekt)](images/sdo01.png)

Weitere Informationen finden Sie unter [Abrufen von Dienst- und Benutzer-SDOs.](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos)

Die zweite Möglichkeit, auf die Objekte Zugriff auf andere Objekte gewähren, besteht darin, dass eine Objektauflistung als Eigenschaft des Objekts dargestellt wird, das sie enthält. Um eine Objektauflistung abzurufen, rufen [**Sie ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) für die -Eigenschaft eines Objekts auf, das die Auflistung darstellt. Um beispielsweise die Policies-Auflistung abzurufen, rufen **Sie ISdo::GetProperty** für die [**ISdo-Schnittstelle**](/windows/desktop/api/sdoias/nn-sdoias-isdo) auf, die vom NPS-Objekt verfügbar gemacht wird.

> [!Note]  
> Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt.

 

![Abrufen der Richtliniensammlung](images/sdo02.png)

Beispielcode zum Abrufen der Richtlinienauflistung finden Sie unter [Abrufen einer Sammlung.](/windows/desktop/Nps/sdo-retrieving-a-collection)

Das [**NPS-Serverdatenobjekt**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) verfügt über die folgenden Eigenschaften, die Auflistungen darstellen:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Revisionsstelle
</dt> <dd>

Der einzige Prüfer in der Prüfersammlung ist das [**NT-Ereignisprotokoll**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Politik
</dt> <dd>

Jedes [**Richtlinienobjekt**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) verfügt über eine -Eigenschaft, die eine Auflistung von Bedingungen darstellt.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profile
</dt> <dd>

Jedes [**Profilobjekt**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in den Profiles-Auflistungen verfügt über eine -Eigenschaft, die eine Attributauflistung darstellt. Eine Liste der von [SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) unterstützten Attribute finden Sie unter Unterstützte SDO-Attribute.

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protokolle
</dt> <dd>

Die protocols-Auflistung enthält das RADIUS-Protokollobjekt, das eine Clientssammlung enthält, die RADIUS-Clients darstellt. Beispielcode zum Abrufen [der Clientsammlung](/windows/desktop/Nps/sdo-adding-a-client) finden Sie unter Hinzufügen eines Clients.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxyrichtlinien
</dt> <dd>

Diese Sammlung enthält Netzwerkzugriffsrichtlinien, die für die Verarbeitung von Verbindungsanforderungen verwendet werden.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxyprofile
</dt> <dd>

Diese Auflistung enthält Profile, die für die Verarbeitung von Verbindungsanforderungen verwendet werden.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS-Servergruppen
</dt> <dd>

Jede [**RADIUS-Servergruppe**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in der RADIUS-Servergruppenauflistung verfügt über eine -Eigenschaft, die die Auflistung der Server in dieser Servergruppe darstellt.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Anforderungshandler
</dt> <dd>

Diese Sammlung enthält die Sammlung "Microsoft Realms Evaluator". Die Einstellungen "Microsoft NT SAM Authentication" und "Microsoft Accounting" sind ebenfalls in dieser Sammlung verfügbar.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDO-Objekte und -Eigenschaften](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Von SDO unterstützte Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 
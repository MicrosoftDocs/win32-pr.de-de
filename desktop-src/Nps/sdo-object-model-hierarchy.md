---
title: Objektmodell Hierarchie
description: Die Objekte im SDO-Objektmodell werden in einer Hierarchie angeordnet. Dies bedeutet, dass Objekte in SDO auf andere Objekte in SDO zugreifen können.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390597"
---
# <a name="object-model-hierarchy"></a>Objektmodell Hierarchie

Die Objekte im SDO-Objektmodell werden in einer Hierarchie angeordnet. Dies bedeutet, dass Objekte in SDO auf andere Objekte in SDO zugreifen können.

-Objekte ermöglichen den Zugriff auf andere-Objekte auf zwei Arten. Eine Möglichkeit besteht darin, dass das-Objekt eine Schnittstelle verfügbar macht, die Methoden zum Abrufen anderer Objekte bereitstellt. Ein Beispiel für diesen Ansatz ist das Computer Objekt. Das Computer Objekt macht die [**isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) -Schnittstelle verfügbar. Die [**isdomachine:: getservicesdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) -Methode ruft ein Dienst Objekt ab. Die [**isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) -Methode ruft ein Benutzerobjekt ab.

![Computer Objekt, das die isdomachine-Schnittstelle](images/sdo01.png)

Weitere Informationen finden Sie unter Abrufen von [Dienst-und Benutzer-SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).

Die zweite Möglichkeit, dass Objekte auf andere Objekte zugreifen, besteht darin, dass eine Objekt Auflistung als Eigenschaft des Objekts dargestellt wird, in dem Sie enthalten ist. Rufen Sie zum Abrufen einer Objekt Auflistung [**isdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) für die-Eigenschaft eines Objekts auf, das die Auflistung darstellt. Um z. b. die Richtlinien Auflistung abzurufen, rufen Sie **isdo:: GetProperty** in der [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle auf, die vom NPS-Objekt verfügbar gemacht wird.

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.

 

![Abrufen der Richtlinien Sammlung](images/sdo02.png)

Beispielcode, der die Richtlinien Auflistung abruft, finden Sie unter [Abrufen einer](/windows/desktop/Nps/sdo-retrieving-a-collection)Auflistung.

Das [**NPS-Server Datenobjekt**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) verfügt über die folgenden Eigenschaften, die Sammlungen darstellen:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Rechnung
</dt> <dd>

Der einzige Auditor in der Prüfer Sammlung ist das [**NT-Ereignisprotokoll**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies
</dt> <dd>

Jedes [**Richtlinien Objekt**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) verfügt über eine-Eigenschaft, die eine Auflistung von Bedingungen darstellt.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Liert
</dt> <dd>

Jedes [**Profil Objekt**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in den Profil Auflistungen verfügt über eine-Eigenschaft, die eine Attribut Auflistung darstellt. Eine Liste der Attribute, die von SDO unterstützt werden, finden [Sie unter Unterstützte SDO-Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes) .

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protokollen
</dt> <dd>

Die Protokolle-Auflistung enthält das RADIUS-Protokoll Objekt, das eine Clients-Sammlung enthält, die RADIUS-Clients darstellt. Siehe [Hinzufügen eines Clients](/windows/desktop/Nps/sdo-adding-a-client) für Beispielcode, der zeigt, wie die Client Auflistung abgerufen wird.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Richtlinien
</dt> <dd>

Diese Sammlung enthält Netzwerk Zugriffsrichtlinien, die für die Verarbeitung von Verbindungsanforderungen verwendet werden.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy profile
</dt> <dd>

Diese Sammlung enthält Profile, die für die Verarbeitung von Verbindungsanforderungen verwendet werden.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS-Server Gruppen
</dt> <dd>

Jede [**RADIUS-Server Gruppe**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in der RADIUS-Server Gruppen Auflistung verfügt über eine-Eigenschaft, die die Sammlung der Server in dieser Server Gruppe darstellt.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Anforderungs Handler
</dt> <dd>

Diese Sammlung enthält die "Microsoft Realm Evaluator"-Sammlung. Die Einstellungen "Microsoft NT Sam-Authentifizierung" und "Microsoft Accounting" sind auch in dieser Sammlung verfügbar.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDO-Objekte und-Eigenschaften](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Unterstützte SDO-Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 
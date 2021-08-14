---
description: Ermöglicht den Zugriff auf die Richtlinieninformationen einer Erweiterung.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: PolicyInformation-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fa717361ac5cb270eb61f0199b92cb801a46fabd143a9dd1ed26e43e23383657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978571"
---
# <a name="policyinformation-object"></a>PolicyInformation-Objekt

\[Das **PolicyInformation-Objekt** kann in den betriebssystemen verwendet werden, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatrichtlinien verwenden, um Richtlinieninformationen in der Zertifikatrichtlinienerweiterung zu verarbeiten.\]

Das **PolicyInformation-Objekt** bietet Zugriff auf die Richtlinieninformationen einer Erweiterung.

## <a name="when-to-use"></a>Verwendung

Das **PolicyInformation-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Rufen Sie die Richtlinien-OID ab.
-   Ruft eine Auflistung der Qualifizierer der Richtlinie ab.

## <a name="members"></a>Member

Das **PolicyInformation-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **PolicyInformation-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | BESCHREIBUNG                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Oid**](policyinformation-oid.md)<br/>               | Ruft die OID der Richtlinie [](oid.md) als OID-Objekt ab. Dies ist die Standardeigenschaft.<br/>       |
| [**Qualifikation**](policyinformation-qualifiers.md)<br/> | Ruft eine Auflistung der Qualifizierer der Richtlinie als [**Qualifiziererobjekt**](qualifiers.md) ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **PolicyInformation-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

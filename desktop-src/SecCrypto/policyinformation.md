---
description: Bietet Zugriff auf die Richtlinien Informationen einer Erweiterung.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Policyinformation-Objekt
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
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364801"
---
# <a name="policyinformation-object"></a>Policyinformation-Objekt

\[Das **policyinformation** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung zu verarbeiten.\]

Das **policyinformation** -Objekt ermöglicht den Zugriff auf die Richtlinien Informationen einer Erweiterung.

## <a name="when-to-use"></a>Verwendung

Das **policyinformation** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Rufen Sie die Richtlinie OID ab.
-   Ruft eine Auflistung der Qualifizierer der Richtlinie ab.

## <a name="members"></a>Member

Das **policyinformation** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **policyinformation** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                      | BESCHREIBUNG                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**OID**](policyinformation-oid.md)<br/>               | Ruft die OID der Richtlinie als [**OID**](oid.md) -Objekt ab. Dies ist die Standard Eigenschaft.<br/>       |
| [**Qualifikation**](policyinformation-qualifiers.md)<br/> | Ruft eine Auflistung der Qualifizierer der Richtlinie als [**qualifiziererobjekt**](qualifiers.md) ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **policyinformation** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

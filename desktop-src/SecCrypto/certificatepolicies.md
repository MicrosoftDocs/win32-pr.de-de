---
description: Eine Auflistung von PolicyInformation-Objekten.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: CertificatePolicies-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8da0ad9681f3dd87227a7fe0b5a5419ceac4c7ee354fb1548427c100561e816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770839"
---
# <a name="certificatepolicies-object"></a>CertificatePolicies-Objekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikatrichtlinien verwenden, um die Zertifikatrichtlinien abzurufen.\]

Das **CertificatePolicies-Objekt** stellt eine Auflistung von [**PolicyInformation-Objekten**](policyinformation.md) dar. Jedes [**PolicyInformation-Objekt**](policyinformation.md) stellt eine einzelne Zertifikatrichtlinie dar.

## <a name="when-to-use"></a>Verwendung

Das **CertificatePolicies-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der Zertifikatrichtlinien in der Auflistung ab.
-   Rufen Sie ein bestimmtes [**PolicyInformation-Objekt**](policyinformation.md) aus der Auflistung ab.
-   Durchlaufen sie die Auflistung.

## <a name="members"></a>Member

Das **CertificatePolicies-Objekt** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **CertificatePolicies-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                    | Zugriffstyp          | Beschreibung                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](certificatepolicies-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**PolicyInformation-Objekte**](policyinformation.md) in der Auflistung ab.<br/>                                                                                                                    |
| [**Element**](certificatepolicies-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**PolicyInformation-Objekt**](policyinformation.md) ab, das die indizierte Zertifikatrichtlinie der Auflistung darstellt. Dies ist die Standardeigenschaft.<br/>                                                    |



 

## <a name="remarks"></a>Hinweise

Das **CertificatePolicies-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

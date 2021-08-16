---
description: Stellt eine Auflistung von Qualifizierern dar.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Qualifiziererobjekt (Iads.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f68dbeefefbe675199522dfbc5b1dab81b8a2840fa8b7d5189c72b811fcba7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900956"
---
# <a name="qualifiers-object"></a>Qualifiziererobjekt

\[Das **Qualifiziererobjekt** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatrichtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinieninformationen in der Zertifikatrichtlinienerweiterung sind.\]

Das **Qualifiziererobjekt** stellt eine Auflistung von Qualifizierern dar.

## <a name="when-to-use"></a>Verwendung

Das **Qualifizierer-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft eine bestimmte erweiterte Eigenschaft aus der Auflistung ab.
-   Ruft die Anzahl der erweiterten Eigenschaften in der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Qualifizierer-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Qualifizierer-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](qualifiers-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der Qualifizierer in der Auflistung ab.<br/>                                                                                                                                                                |
| [**Element**](qualifiers-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**Qualifiziererobjekt**](qualifier.md) ab, das den indizierten Qualifizierer der Auflistung darstellt. Dies ist die Standardeigenschaft.<br/>                                                                             |



 

## <a name="remarks"></a>Hinweise

Das **Qualifiziererobjekt** kann nicht erstellt werden.

Die [**CAPICOM-Objekteigenschaft PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) gibt ein **Qualifizierer-Objekt** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| Header<br/>          | <dl> <dt>Iads.h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

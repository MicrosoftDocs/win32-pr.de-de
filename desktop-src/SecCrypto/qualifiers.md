---
description: Stellt eine Auflistung von Qualifizierern dar.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Qualifiziererobjekt (IADs. h)
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
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358348"
---
# <a name="qualifiers-object"></a>Qualifiziererobjekt

\[Das **qualifiziererobjekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]

Das **qualifiziererobjekt** stellt eine Auflistung von Qualifizierern dar.

## <a name="when-to-use"></a>Verwendung

Das **qualifiziererobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft eine bestimmte erweiterte Eigenschaft aus der Auflistung ab.
-   Ruft die Anzahl der erweiterten Eigenschaften in der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **qualifiziererobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **qualifiziererobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](qualifiers-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](qualifiers-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der Qualifizierer in der Auflistung ab.<br/>                                                                                                                                                                |
| [**Element**](qualifiers-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**qualifiziererobjekt**](qualifier.md) ab, das den indizierten Qualifizierer der Auflistung darstellt. Dies ist die Standard Eigenschaft.<br/>                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Das **qualifiziererobjekt** kann nicht erstellt werden.

Die [**policyinformation. Qualifizierer**](policyinformation-qualifiers.md) CAPICOM-Objekt Eigenschaft gibt ein **qualifiziererobjekt** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| Header<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

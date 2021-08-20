---
description: Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Qualifizierer für Benutzerhinweise dar.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Qualifiziererobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 546a4ea5fea67dc386d789f80437fddf7d08c886f9255e6cd09378f2d5bf7e23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975726"
---
# <a name="qualifier-object"></a>Qualifiziererobjekt

\[Das **Qualifiziererobjekt** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikatrichtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinieninformationen in der Zertifikatrichtlinienerweiterung sind.\]

Das **Qualifier-Objekt** stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzerhinweisqualifizierer dar.

## <a name="when-to-use"></a>Verwendung

Das **Qualifiziererobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft den Objektbezeichner des Qualifizierers ab.
-   Rufen Sie den Uniform Resource Identifier (URI) ab, der auf einen von der [*Zertifizierungsstelle*](../secgloss/c-gly.md) veröffentlichten CPS verweist.
-   Rufen Sie den Namen der Organisation ab, die dem Qualifizierer zugeordnet ist.
-   Rufen Sie den Namen und den Inhalt eines Benutzerhinweises ab.

## <a name="members"></a>Member

Das **Qualifiziererobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Qualifiziererobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Zugriffstyp          | Beschreibung                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den URI enthält, der auf einen von der Zertifizierungsstelle veröffentlichten CPS verweist.<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Inhalt des Benutzerhinweises enthält. Diese Eigenschaft ist möglicherweise leer.<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | Schreibgeschützt<br/> | Ruft ein **NoticeNumbers-Objekt** ab, das die Auflistung von Benutzerhinweisnummern enthält. Diese Eigenschaft ist möglicherweise leer.<br/>    |
| [**Oid**](qualifier-oid.md)<br/>                           | Schreibgeschützt<br/> | Ruft ein [**OID-Objekt**](oid.md) ab, das den Qualifizierer identifiziert. Dies ist die Standardeigenschaft.<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Namen der Organisation enthält, die dem Qualifizierer zugeordnet ist. Diese Eigenschaft ist möglicherweise leer.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **Qualifiziererobjekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

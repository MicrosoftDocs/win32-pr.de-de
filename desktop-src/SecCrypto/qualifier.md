---
description: Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzer Hinweis Qualifizierer dar.
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
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358107"
---
# <a name="qualifier-object"></a>Qualifiziererobjekt

\[Das **qualifiziererobjekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]

Das **qualifiziererobjekt** stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzer Hinweis Qualifizierer dar.

## <a name="when-to-use"></a>Verwendung

Das **qualifiziererobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft den Objekt Bezeichner des Qualifizierers ab.
-   Rufen Sie die Uniform Resource Identifier (URI) ab, die auf eine von der Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) veröffentlichte CPS verweist.
-   Ruft den Namen der dem Qualifizierer zugeordneten Organisation ab.
-   Rufen Sie den Namen und den Inhalt einer Benutzer Benachrichtigung ab.

## <a name="members"></a>Member

Das **qualifiziererobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **qualifiziererobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Zugriffstyp          | BESCHREIBUNG                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**Cpspointer**](qualifier-cpspointer.md)<br/>             | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den URI enthält, der auf ein von der Zertifizierungsstelle veröffentlichtes CPS verweist.<br/>                                       |
| [**Explizertext**](qualifier-explicittext.md)<br/>         | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Inhalt der Benutzer Benachrichtigung enthält. Diese Eigenschaft ist möglicherweise leer.<br/>                             |
| [**Benachrichtifür Notierungen**](qualifier-noticenumbers.md)<br/>       | Schreibgeschützt<br/> | Ruft ein **noticenumbers** -Objekt ab, das die Auflistung der Benutzer Hinweis Nummern enthält. Diese Eigenschaft ist möglicherweise leer.<br/>    |
| [**OID**](qualifier-oid.md)<br/>                           | Schreibgeschützt<br/> | Ruft ein [**OID**](oid.md) -Objekt ab, das den Qualifizierer identifiziert. Dies ist die Standard Eigenschaft.<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Namen der dem Qualifizierer zugeordneten Organisation enthält. Diese Eigenschaft ist möglicherweise leer.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **qualifiziererobjekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

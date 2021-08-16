---
description: Stellt die Zertifikaterweiterungsvorlage des Zertifikats dar.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Vorlagenobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 53c7b06fa4194d0adb4124f3978787f5d1fce0ba88e78ef99dcd6ac162eca2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897321"
---
# <a name="template-object"></a>Vorlagenobjekt

\[Das **Template-Objekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikatvorlage verwenden, um die Zertifikaterweiterungsvorlage abzurufen.\]

Das **Template-Objekt** stellt die Zertifikaterweiterungsvorlage des Zertifikats dar.

## <a name="when-to-use"></a>Verwendung

Das **Template-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Bestimmen Sie, ob die Vorlage als kritisch oder vorhanden markiert ist.
-   Rufen Sie den [*Objektbezeichner*](../secgloss/o-gly.md) (OID) oder den Namen der Vorlage ab.
-   Rufen Sie die Neben- oder Hauptversion der Vorlage ab.

## <a name="members"></a>Member

Das **Template-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Template-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                 | Zugriffstyp          | Beschreibung                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Vorlagenerweiterung als kritisch markiert ist.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Vorlagenerweiterung vorhanden ist.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Schreibgeschützt<br/> | Ruft die Hauptversionsnummer der Vorlage ab.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Schreibgeschützt<br/> | Ruft die Nebenversionsnummer der Vorlage ab.<br/>                                         |
| [**Name**](template-name.md)<br/>                 | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Namen der Vorlage enthält.<br/>                                  |
| [**Oid**](template-oid.md)<br/>                   | Schreibgeschützt<br/> | Ruft ein [**OID-Objekt**](oid.md) ab, das das **Template-Objekt** identifiziert.<br/>             |



 

## <a name="remarks"></a>Hinweise

Das **Template-Objekt** kann nicht erstellt werden.

Ein **Template-Objekt** wird von der [**Certificate.Template-Methode**](certificate-template.md) zurückgegeben.

CAPICOM verwendet zwei verschiedene Versionen von Zertifikatvorlagen. Die folgende Tabelle zeigt den Namen und die OID für jede Zertifikatvorlagenversion.



| Version | Name                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | szOID \_ ENROLL \_ CERTTYPE \_ EXTENSION | "1.3.6.1.4.1.311.20.2" |
| V2      | \_SZOID-ZERTIFIKATVORLAGE \_       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

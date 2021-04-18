---
description: Stellt die Zertifikat Erweiterungs Vorlage des Zertifikats dar.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Vorlagen Objekt
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
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371232"
---
# <a name="template-object"></a>Vorlagen Objekt

\[Das **Vorlagen** Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]

Das **Vorlagen** Objekt stellt die Zertifikat Erweiterungs Vorlage des Zertifikats dar.

## <a name="when-to-use"></a>Verwendung

Das **Vorlagen** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Bestimmen Sie, ob die Vorlage als kritisch oder vorhanden markiert ist.
-   Rufen Sie die [*Objekt Kennung*](../secgloss/o-gly.md) (OID) oder den Namen der Vorlage ab.
-   Rufen Sie die neben Version oder die Hauptversion der Vorlage ab.

## <a name="members"></a>Member

Das **Vorlagen** Objekt enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Vorlagen** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                 | Zugriffstyp          | BESCHREIBUNG                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung als kritisch markiert ist.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung vorhanden ist.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Schreibgeschützt<br/> | Ruft die Hauptversionsnummer der Vorlage ab.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Schreibgeschützt<br/> | Ruft die neben Versionsnummer der Vorlage ab.<br/>                                         |
| [**Name**](template-name.md)<br/>                 | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Namen der Vorlage enthält.<br/>                                  |
| [**OID**](template-oid.md)<br/>                   | Schreibgeschützt<br/> | Ruft ein [**OID**](oid.md) -Objekt ab, das das **Vorlagen** Objekt identifiziert.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Das **Vorlagen** Objekt kann nicht erstellt werden.

Ein **Vorlagen** Objekt wird von der [**Certificate. Template**](certificate-template.md) -Methode zurückgegeben.

CAPICOM verwendet zwei unterschiedliche Versionen von Zertifikat Vorlagen. In der folgenden Tabelle werden der Name und die OID für jede Zertifikat Vorlagen Version angezeigt.



| Version | Name                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | szoid \_ ENROLL \_ certtype- \_ Erweiterung | "1.3.6.1.4.1.311.20.2" |
| V2      | szoid- \_ Zertifikat \_ Vorlage       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

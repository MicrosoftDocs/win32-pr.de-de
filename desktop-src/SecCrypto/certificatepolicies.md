---
description: Eine Auflistung von policyinformation-Objekten.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Certificatepolicies-Objekt
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
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369697"
---
# <a name="certificatepolicies-object"></a>Certificatepolicies-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um die Zertifikat Richtlinien abzurufen.\]

Das **certificatepolicies** -Objekt stellt eine Auflistung von [**policyinformation**](policyinformation.md) -Objekten dar. Jedes [**policyinformation**](policyinformation.md) -Objekt stellt eine einzelne Zertifikat Richtlinie dar.

## <a name="when-to-use"></a>Verwendung

Das **certificatepolicies** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Abrufen der Anzahl der Zertifikat Richtlinien in der Sammlung.
-   Rufen Sie ein bestimmtes [**policyinformation**](policyinformation.md) -Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **certificatepolicies** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **certificatepolicies** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                    | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](certificatepolicies-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](certificatepolicies-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**policyinformation**](policyinformation.md) -Objekte in der Auflistung ab.<br/>                                                                                                                    |
| [**Element**](certificatepolicies-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**policyinformation**](policyinformation.md) -Objekt ab, das die indizierte Zertifikat Richtlinie der Auflistung darstellt. Dies ist die Standard Eigenschaft.<br/>                                                    |



 

## <a name="remarks"></a>Bemerkungen

Das **certificatepolicies** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

---
description: Stellt eine einzelne Zertifikat Erweiterung dar.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Erweiterungs Objekt (mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369627"
---
# <a name="extension-object"></a>Erweiterungs Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **Erweiterungs** Objekt stellt eine einzelne Zertifikat Erweiterung dar.

## <a name="when-to-use"></a>Verwendung

Das **Erweiterungs** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Rufen Sie die OID der Zertifikat Erweiterung ab.
-   Abrufen der von einem [**encodeddata**](encodeddata.md) -Objekt dargestellten Zertifikat Erweiterungs Daten.
-   Bestimmen Sie, ob die Zertifikat Erweiterung als kritisch markiert ist.

## <a name="members"></a>Member

Das **Erweiterungs** Objekt enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Erweiterungs** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp          | BESCHREIBUNG                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**Encoddata**](extension-encodeddata.md)<br/> | Schreibgeschützt<br/> | Ruft die codierten Daten für die Erweiterung ab.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.<br/> |
| [**OID**](extension-oid.md)<br/>                 | Schreibgeschützt<br/> | Ruft den Objekt Bezeichner für die Erweiterung ab. Dies ist die Standard Eigenschaft.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Das **Erweiterungs** Objekt kann nicht erstellt werden.

Das **Erweiterungs** Objekt wird vom Erweiterungs Objekt für [**Erweiterungen**](extensions.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>Mmcobj. h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

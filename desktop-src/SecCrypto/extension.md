---
description: Stellt eine einzelne Zertifikaterweiterung dar.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Erweiterungsobjekt (Mmcobj.h)
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
ms.openlocfilehash: e311c6dc69f40d32163c70cabf6a38780a989764bd77f4023c61ede5c1ba713c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006958"
---
# <a name="extension-object"></a>Erweiterungsobjekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **Extension-Objekt** stellt eine einzelne Zertifikaterweiterung dar.

## <a name="when-to-use"></a>Verwendung

Das **Extension-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Rufen Sie die OID der Zertifikaterweiterung ab.
-   Rufen Sie die Durch ein [**EncodedData-Objekt**](encodeddata.md) dargestellten Zertifikaterweiterungsdaten ab.
-   Bestimmen Sie, ob die Zertifikaterweiterung als kritisch markiert ist.

## <a name="members"></a>Member

Das **Extension-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Extension-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp          | BESCHREIBUNG                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**Codierte Daten**](extension-encodeddata.md)<br/> | Schreibgeschützt<br/> | Ruft die codierten Daten für die Erweiterung ab.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.<br/> |
| [**Oid**](extension-oid.md)<br/>                 | Schreibgeschützt<br/> | Ruft den Objektbezeichner für die Erweiterung ab. Dies ist die Standardeigenschaft.<br/>   |



 

## <a name="remarks"></a>Hinweise

Das **Extension-Objekt** kann nicht erstellt werden.

Das **Extension-Objekt** wird vom [**Extensions-Auflistungsobjekt**](extensions.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>Mmcobj.h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

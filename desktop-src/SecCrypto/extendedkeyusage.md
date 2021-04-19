---
description: Bietet schreibgeschützten Zugriff auf die Eigenschaften der erweiterten Schlüssel Verwendung (Extended Key Usage, EKU) eines Zertifikats.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Extendedkeyusage-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367690"
---
# <a name="extendedkeyusage-object"></a>Extendedkeyusage-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **extendedkeyusage** -Objekt bietet schreibgeschützten Zugriff auf die Eigenschaften der erweiterten Schlüssel Verwendung (Extended Key Usage, EKU) eines Zertifikats.

## <a name="members"></a>Member

Das **extendedkeyusage** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **extendedkeyusage** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp          | BESCHREIBUNG                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EKUs**](extendedkeyusage-ekus.md)<br/>             | Schreibgeschützt<br/> | [**EKUs**](ekus.md) -Sammlung, die die [**EKU**](eku.md) -Objekte für das Zertifikat enthält.<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | Schreibgeschützt<br/> | Ruft einen **booleschen** Wert ab, der angibt, ob die EKU-Erweiterung als kritisch markiert ist.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Schreibgeschützt<br/> | Ruft einen **booleschen** Wert ab, der angibt, ob die EKU-Erweiterung vorhanden ist.<br/> Dies ist die Standard Eigenschaft. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **extendedkeyusage** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 

---
description: Bietet schreibgeschützten Zugriff auf die Erweiterten Schlüsselverwendungseigenschaften (Extended Key Usage, EKU) eines Zertifikats.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: ExtendedKeyUsage-Objekt
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
ms.openlocfilehash: 927e219e22bd0e87c444b1ca3cb63b09a5ddc2fb9ac74e63ebb8f66c6ed75437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007318"
---
# <a name="extendedkeyusage-object"></a>ExtendedKeyUsage-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **ExtendedKeyUsage-Objekt** bietet schreibgeschützten Zugriff auf die Eigenschaften der erweiterten Schlüsselverwendung (Extended Key Usage, EKU) eines Zertifikats.

## <a name="members"></a>Member

Das **ExtendedKeyUsage-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ExtendedKeyUsage-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp          | Beschreibung                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EKUs**](extendedkeyusage-ekus.md)<br/>             | Schreibgeschützt<br/> | [**EKUs-Sammlung,**](ekus.md) die die [**EKU-Objekte**](eku.md) für das Zertifikat enthält.<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | Schreibgeschützt<br/> | Ruft einen **booleschen Wert ab,** der angibt, ob die EKU-Erweiterung als kritisch markiert ist.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Schreibgeschützt<br/> | Ruft einen **booleschen Wert ab,** der angibt, ob die EKU-Erweiterung vorhanden ist.<br/> Dies ist die Standardeigenschaft. <br/> |



 

## <a name="remarks"></a>Hinweise

Das **ExtendedKeyUsage-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 

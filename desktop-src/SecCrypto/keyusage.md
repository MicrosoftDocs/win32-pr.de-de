---
description: Bietet schreibgeschützten Zugriff auf Schlüsselverwendungseigenschaften eines Zertifikats.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: KeyUsage-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 37b1e33ccb92b2d46effa9f0575f0331fa064e79d172715b8746355d5e99d2b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622270"
---
# <a name="keyusage-object"></a>KeyUsage-Objekt

\[Das **KeyUsage-Objekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **KeyUsage-Objekt** bietet schreibgeschützten Zugriff auf Schlüsselverwendungseigenschaften eines Zertifikats.

## <a name="members"></a>Member

Das **KeyUsage-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **KeyUsage-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp          | Beschreibung                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die **KeyUsage-Erweiterung** als kritisch markiert ist.<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das CRLSign-Bit festgelegt ist.<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das dataEncipherment-Bit festgelegt ist.<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das decipherOnly-Bit festgelegt ist.<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das digitalSignature-Bit festgelegt ist.<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das encipherOnly-Bit festgelegt ist.<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das keyAgreement-Bit festgelegt ist.<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das keyEncipherment-Bit festgelegt ist.<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das nonRepudiationEnabled-Bit festgelegt ist.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die **KeyUsage-Erweiterung** vorhanden ist.<br/> Dies ist die Standardeigenschaft.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **KeyUsage-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 

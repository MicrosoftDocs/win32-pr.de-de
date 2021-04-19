---
description: Bietet schreibgeschützten Zugriff auf Schlüssel Verwendungs Eigenschaften eines Zertifikats.
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
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357300"
---
# <a name="keyusage-object"></a>KeyUsage-Objekt

\[Das **KeyUsage** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **KeyUsage** -Objekt bietet schreibgeschützten Zugriff auf Schlüssel Verwendungs Eigenschaften eines Zertifikats.

## <a name="members"></a>Member

Das **KeyUsage** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **KeyUsage** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die **KeyUsage** -Erweiterung als kritisch markiert ist.<br/>                                  |
| [**Iscrlsignenabled**](keyusage-iscrlsignenabled.md)<br/>                   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das crlsign-Bit festgelegt ist.<br/>                                                         |
| [**Isdataenciphermentaktivierte**](keyusage-isdataenciphermentenabled.md)<br/> | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das DataEncipherment-Bit festgelegt ist.<br/>                                                |
| [**Isdecocipheronlyaktivierte**](keyusage-isdecipheronlyenabled.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das decodische Bit festgelegt ist.<br/>                                                    |
| [**Isdigitalsignatureaktivierte**](keyusage-isdigitalsignatureenabled.md)<br/> | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das DigitalSignature-Bit festgelegt ist.<br/>                                                |
| [**"Isencipheronlyaktiviert"**](keyusage-isencipheronlyenabled.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das encipheronly-Bit festgelegt ist.<br/>                                                    |
| [**Iskeyagreementaktivierte**](keyusage-iskeyagreementenabled.md)<br/>         | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das KeyAgreement-Bit festgelegt ist.<br/>                                                    |
| [**Iskeycertsignenabled**](keyusage-iskeycertsignenabled.md)<br/>           | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.<br/>                                                     |
| [**Iskeykociphermentaktivierte**](keyusage-iskeyenciphermentenabled.md)<br/>   | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das KeyEncipherment-Bit festgelegt ist.<br/>                                                 |
| [**Isnonablehnt ationaktivierte**](keyusage-isnonrepudiationenabled.md)<br/>     | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob das nonablehnationaktivierte Bit festgelegt ist.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Schreibgeschützt<br/> | Ruft einen booleschen Wert ab, der angibt, ob die **KeyUsage** -Erweiterung vorhanden ist.<br/> Dies ist die Standard Eigenschaft.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **KeyUsage** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 

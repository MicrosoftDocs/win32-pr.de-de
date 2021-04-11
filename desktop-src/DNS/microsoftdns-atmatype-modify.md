---
title: Modify-Methode der MicrosoftDNS_ATMAType-Klasse
description: Die Modify-Methode aktualisiert einen Atma-Ressourcen Eintrag (ATM-Adresse).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_ATMAType-Klasse
- DNS-MicrosoftDNS_ATMAType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040620"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Modify-Methode der MicrosoftDNS \_ atmatype-Klasse

Die **Modify** -Methode aktualisiert einen Atma-Ressourcen Eintrag (ATM-Adresse).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Format* \[ in, optional\]
</dt> <dd>

ATM-Adressformat. Zwei mögliche Werte für das Format sind: 0, was das AESA-Format (ATM End System Address) angibt, und 1 gibt das E. 164-Format an.

</dd> <dt>

*Atmaddress* \[ in, optional\]
</dt> <dd>

Zeichenfolge mit variabler Länge von Oktetten, die die ATM-Adresse des Knotens bzw. Besitzers enthält, auf den sich diese RR bezieht. Die ersten vier Bytes des Arrays werden verwendet, um die Größe der Oktett-Zeichenfolge zu speichern. Das signifikanteste Byte wird in Byte 0 gespeichert.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das neue-Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ atmatype**](microsoftdns-atmatype.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS \_ atmatype-Klasse**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






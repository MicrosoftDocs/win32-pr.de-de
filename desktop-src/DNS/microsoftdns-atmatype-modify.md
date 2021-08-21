---
title: Modify-Methode der MicrosoftDNS_ATMAType Klasse
description: Die Modify-Methode aktualisiert einen ATM-Adress-ressourcendatensatz (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_ATMAType class
- MicrosoftDNS_ATMAType DNS-Klasse, Modify-Methode
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
ms.openlocfilehash: f3c8f98288c519340e6a95959964a4c42799201c7e1701bb748f634746a94226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163758"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Modify-Methode der MicrosoftDNS \_ ATMAType-Klasse

Die **Modify-Methode** aktualisiert einen ATM-Adress-ressourcendatensatz (ATMA).

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

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Formatieren* \[ in, optional\]
</dt> <dd>

ATM-Adressformat. Zwei mögliche Werte für FORMAT sind: 0 , das das Format der ATM-Endsystemadresse (ATM End System Address, AESA) angibt, und 1 das E.164-Format.

</dd> <dt>

*ATMAddress* \[ in, optional\]
</dt> <dd>

Zeichenfolge variabler Länge von Oktetten, die die ATM-Adresse des Knotens/Besitzers enthalten, auf den sich diese RR bezieht. Die ersten vier Bytes des Arrays werden verwendet, um die Größe der Oktettzeichenfolge zu speichern. Das wichtigste Byte wird in Byte 0 gespeichert.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Nicht angegebene Parameter bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ ATMAType-Klasse**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






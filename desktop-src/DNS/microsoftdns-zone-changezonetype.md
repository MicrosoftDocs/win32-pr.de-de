---
title: Changezonetype-Methode der MicrosoftDNS_Zone-Klasse
description: Die changezonetype-Methode ändert den Typ einer Zone.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- Changezonetype-Methode (DNS)
- Changezonetype-Methode, DNS, MicrosoftDNS_Zone-Klasse
- MicrosoftDNS_Zone-Klasse DNS, changezonetype-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040486"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse

Die **changezonetype** -Methode ändert den Typ einer Zone.

## <a name="syntax"></a>Syntax


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zonetype* \[ in\]
</dt> <dd>

Zonentyp. Folgende Werte sind gültig:



| Wert                                                                        | Bedeutung                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Primäre Zone<br/>   |
| <dl> <dt>1</dt> </dl> | Sekundäre Zone.<br/> |
| <dl> <dt>2</dt> </dl> | Stub-Zone.<br/>      |
| <dl> <dt>3</dt> </dl> | Zonen Weiterleitung.<br/> |



 

</dd> <dt>

*DataFileName* \[ in, optional\]
</dt> <dd>

Der Name der Datendatei, die der Zone zugeordnet ist.

</dd> <dt>

*Ipaddr* \[ in, optional\]
</dt> <dd>

Die IP-Adresse des Mater-DNS-Servers für die Zone.

</dd> <dt>

*Adminemailname* \[ in, optional\]
</dt> <dd>

E-Mail-Adresse des Administrators, der für die Zone zuständig ist.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

RR vom Typ **MicrosoftDNS \_ Zone**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Zone**](microsoftdns-zone.md)
</dt> <dt>

[**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 






---
title: Die Methode "kreatezone" der MicrosoftDNS_Zone-Klasse
description: Die Methode "kreatezone" erstellt eine DNS-Zone.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Methode der Methode "kreatezone"
- Methode der Methoden-DNS, MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, Methode "kreatezone"
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040784"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse

Die Methode " **kreatezone** " erstellt eine DNS-Zone.

## <a name="syntax"></a>Syntax


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zonenname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Zone darstellt.

</dd> <dt>

*Zonetype* \[ in\]
</dt> <dd>

Zonentyp. Folgende Werte sind gültig:



| Wert                                                                        | Bedeutung                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | AD integriert.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Sekundäre Zone.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Stub-Zone.<br/> **Windows Server 2003:** Dieser Zonentyp wird in Windows Server 2003 eingeführt.<br/>      |
| <dl> <dt>4</dt> </dl> | Zonen Weiterleitung.<br/> **Windows Server 2003:** Dieser Zonentyp wird in Windows Server 2003 eingeführt.<br/> |



 

</dd> <dt>

*Dsintegriert* \[ in\]
</dt> <dd>

Gibt an, ob Zonendaten in der Active Directory oder in Dateien gespeichert werden. Wenn der Wert true ist, werden die Daten in der Active Directory gespeichert. Wenn der Wert false ist, werden die Daten in Dateien gespeichert.

</dd> <dt>

*DataFileName* \[ in, optional\]
</dt> <dd>

Der Name der Datendatei, die der Zone zugeordnet ist.

</dd> <dt>

*Ipaddr* \[ in, optional\]
</dt> <dd>

Die IP-Adresse des DNS-Master Servers für die Zone.

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

[**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-changezonetype.md)
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

 

 






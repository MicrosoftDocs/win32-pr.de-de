---
title: Modify-Methode der MicrosoftDNS_WINSType-Klasse
description: Die Modify-Methode aktualisiert einen Windows Internet Name Service (WINS)-Ressourcen Daten Satz.
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_WINSType-Klasse
- DNS-MicrosoftDNS_WINSType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859041"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Modify-Methode der MicrosoftDNS- \_ winstype-Klasse

Die **Modify** -Methode aktualisiert einen Windows Internet Name Service (WINS)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Mappingflag* \[ in, optional\]
</dt> <dd>

WINS-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen. Die folgenden Werte sind gültig.



| Wert                                                                                                                                               | Bedeutung                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Replikationsflag<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag "keine Replikation (lokaler Datensatz)"<br/> |



 

</dd> <dt>

*Lookuptimeout* \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die ein DNS-Server versucht, mithilfe von WINS eine Auflösung durchsuchen zu können.

</dd> <dt>

*Cachetimeout* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, für die ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.

</dd> <dt>

*Windows Server* \[ in, optional\]
</dt> <dd>

Liste mit durch Trennzeichen getrennten IP-Adressen von WINS-Servern, die in WINS-suchen verwendet werden.

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

[**MicrosoftDNS \_ winstype**](microsoftdns-winstype.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ winstype-Klasse**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






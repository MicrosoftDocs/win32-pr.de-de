---
title: Modify-Methode der MicrosoftDNS_SRVType-Klasse
description: Die Modify-Methode aktualisiert einen Dienst Ressourcen Daten Satz (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_SRVType-Klasse
- DNS-MicrosoftDNS_SRVType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040939"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Modify-Methode der MicrosoftDNS \_ srvtype-Klasse

Die **Modify** -Methode aktualisiert einen Dienst Ressourcen Daten Satz (SRV).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Priorität* \[ in, optional\]
</dt> <dd>

Priorität des im Besitzer Namen angegebenen Zielhosts. Niedrigere Zahlen implizieren höhere Prioritäten.

</dd> <dt>

*Gewichtung* \[ in, optional\]
</dt> <dd>

Gewichtung des Zielhosts. Dies ist hilfreich bei der Auswahl zwischen Hosts mit der gleichen Priorität. Die Wahrscheinlichkeit, diesen Host zu verwenden, sollte proportional zu seiner Gewichtung sein.

</dd> <dt>

*Port* \[ in, optional\]
</dt> <dd>

Port, der auf dem Zielhost eines Protokoll Diensts verwendet wird.

</dd> <dt>

*Srvdomainname* \[ in, optional\]
</dt> <dd>

Der voll qualifizierte Namen des Zielhosts. Ein Ziel von \\ . \\ bedeutet, dass der Dienst in dieser Domäne nicht verfügbar ist.

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

[**MicrosoftDNS- \_ srvtype**](microsoftdns-srvtype.md)
</dt> <dt>

[**Die Methode "kreateinstancefrompropertydata" der Klasse "srvtype" von MicrosoftDNS \_**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






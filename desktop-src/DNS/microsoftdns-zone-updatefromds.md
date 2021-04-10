---
title: Updatefromds-Methode der MicrosoftDNS_Zone-Klasse
description: Die updatefromds-Methode erzwingt ein Update der Zone aus dem Verzeichnisdienst (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- Updatefromds-Methode (DNS)
- Updatefromds-Methode, DNS, MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, updatefromds-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106569"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse

Die **updatefromds** -Methode erzwingt ein Update der Zone aus dem Verzeichnisdienst (DS).

## <a name="syntax"></a>Syntax


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Damit diese Methode erfolgreich ausgeführt werden kann, muss zonetype NULL sein, und die Zone muss auf dem DS gespeichert werden.

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

[**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 






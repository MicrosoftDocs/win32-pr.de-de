---
title: UpdateFromDS-Methode der MicrosoftDNS_Zone-Klasse
description: Die UpdateFromDS-Methode erzwingt ein Update der Zone vom Verzeichnisdienst (Directory Service, DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- DNS-Methode "UpdateFromDS"
- Dns-, MicrosoftDNS_Zone-Klasse der UpdateFromDS-Methode
- MicrosoftDNS_Zone-Klasse DNS, UpdateFromDS-Methode
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
ms.openlocfilehash: ca537c6440ae14d0e15dea28f62bdb919f3ed7e3348f3a64a2339e0668b5c8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957189"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>UpdateFromDS-Methode der MicrosoftDNS \_ Zone-Klasse

Die **UpdateFromDS-Methode** erzwingt ein Update der Zone vom Verzeichnisdienst (Directory Service, DS).

## <a name="syntax"></a>Syntax


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode erfolgreich auszuführen, muss ZoneType 0 (null) sein, und die Zone muss im DS gespeichert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MicrosoftDNS-Zone**](microsoftdns-zone.md)
</dt> <dt>

[**AgeAllRecords-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**ChangeZoneType-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**CreateZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**PauseZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**ReloadZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**ResetSecondaries-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**ResumeZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**WriteBackZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 






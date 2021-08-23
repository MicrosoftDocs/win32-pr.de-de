---
description: Die FeatureCost-Eigenschaft des Session-Objekts gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Byte) zurück, die für das angegebene Feature und seine übergeordneten Features (bis zum Stamm der Featuretabelle) erforderlich ist.
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session.FeatureCost(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629290"
---
# <a name="sessionfeaturecost-property"></a>Session.FeatureCost(Eigenschaft)

Die **FeatureCost-Eigenschaft** des [**Session-Objekts**](session-object.md) gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Byte) zurück, die für das angegebene Feature und seine übergeordneten Features (bis zum Stamm der Featuretabelle) erforderlich ist. Für jedes Feature werden die Gesamtkosten aus den Datenträgerkosten der einzelnen Komponenten, die mit dem Feature verknüpft sind, zusammengerechnet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession ist als \_ 000C109E-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                             |



 

 





---
description: Die featurecost-Eigenschaft des Session-Objekts gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Bytes) zurück, die für die angegebene Funktion und ihre übergeordneten Funktionen erforderlich ist (bis zum Stamm der Funktions Tabelle).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session. featurecost-Eigenschaft
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
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370166"
---
# <a name="sessionfeaturecost-property"></a>Session. featurecost-Eigenschaft

Die **featurecost** -Eigenschaft des [**Session**](session-object.md) -Objekts gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Bytes) zurück, die für die angegebene Funktion und ihre übergeordneten Funktionen erforderlich ist (bis zum Stamm der Funktions Tabelle). Für jede Funktion werden die Gesamtkosten aus den Datenträger Kosten der einzelnen mit dem Feature verknüpften Komponenten zusammengeführt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





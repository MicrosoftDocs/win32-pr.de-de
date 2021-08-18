---
description: Die FeatureCurrentState-Eigenschaft des Session-Objekts ist eine schreibgeschützte Eigenschaft, die den aktuellen installierten Zustand des angegebenen Features zurückgibt. Zustandswerte finden Sie in der FeatureRequestState-Eigenschaft.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Session.FeatureCurrentState-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3738a33d2c7a855abe6cc60139286b3e9c4d586bc6c2d9d436390fc5e52f4fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629230"
---
# <a name="sessionfeaturecurrentstate-property"></a>Session.FeatureCurrentState-Eigenschaft

Die **FeatureCurrentState-Eigenschaft** des [**Session-Objekts**](session-object.md) ist eine schreibgeschützte Eigenschaft, die den aktuellen installierten Zustand des angegebenen Features zurückgibt. Zustandswerte finden Sie in der [**FeatureRequestState-Eigenschaft.**](session-featurerequeststate.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichenfolgenname der angeforderten Funktion und ein Primärschlüssel in der [Featuretabelle](feature-table.md).

## <a name="remarks"></a>Hinweise

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sitzungskonsistenz**](session-object.md)
</dt> <dt>

[**FeatureRequestState-Eigenschaft**](session-featurerequeststate.md)
</dt> </dl>

 

 





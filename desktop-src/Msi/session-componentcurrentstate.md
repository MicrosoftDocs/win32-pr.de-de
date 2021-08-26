---
description: Die ComponentCurrentState-Eigenschaft des Session-Objekts ist eine schreibgeschützte Eigenschaft, die den aktuellen installierten Zustand der angegebenen Komponente zurückgibt. Zustandswerte finden Sie in der ComponentRequestState-Eigenschaft.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Session.ComponentCurrentState-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ce060c7eddb76491480f4a1de9f477629da489ae9d8412adc02da25b8d7a0a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039857"
---
# <a name="sessioncomponentcurrentstate-property"></a>Session.ComponentCurrentState-Eigenschaft

Die **ComponentCurrentState-Eigenschaft** des [**Session-Objekts**](session-object.md) ist eine schreibgeschützte Eigenschaft, die den aktuellen installierten Zustand der angegebenen Komponente zurückgibt. Zustandswerte finden Sie in der [**ComponentRequestState-Eigenschaft.**](session-componentrequeststate.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichenfolgenname der angeforderten Komponente, Primärschlüssel in der Tabelle Komponente.

## <a name="remarks"></a>Hinweise

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzungskonsistenz**](session-object.md)
</dt> <dt>

[**ComponentRequestState-Eigenschaft**](session-componentrequeststate.md)
</dt> </dl>

 

 





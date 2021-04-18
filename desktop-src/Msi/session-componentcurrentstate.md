---
description: Bei der componentcurrentstate-Eigenschaft des Session-Objekts handelt es sich um eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Komponente zurückgibt. Informationen zu Zustands Werten finden Sie unter der componentrequeststate-Eigenschaft.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Session. componentcurrentstate-Eigenschaft
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
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368474"
---
# <a name="sessioncomponentcurrentstate-property"></a>Session. componentcurrentstate-Eigenschaft

Bei der **componentcurrentstate** -Eigenschaft des [**Session**](session-object.md) -Objekts handelt es sich um eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Komponente zurückgibt. Informationen zu Zustands Werten finden Sie unter der [**componentrequeststate**](session-componentrequeststate.md) -Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichen folgen Name der angeforderten Komponente, Primärschlüssel in der Komponenten Tabelle.

## <a name="remarks"></a>Bemerkungen

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session-object.md)
</dt> <dt>

[**Componentrequeststate (Eigenschaft)**](session-componentrequeststate.md)
</dt> </dl>

 

 





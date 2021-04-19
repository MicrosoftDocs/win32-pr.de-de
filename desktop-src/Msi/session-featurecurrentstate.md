---
description: Die featurecurrentstate-Eigenschaft des Session-Objekts ist eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Funktion zurückgibt. Informationen zu Zustands Werten finden Sie unter der Eigenschaft "featurerequeststate".
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Session. featurecurrentstate (Eigenschaft)
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
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359411"
---
# <a name="sessionfeaturecurrentstate-property"></a>Session. featurecurrentstate (Eigenschaft)

Die **featurecurrentstate** -Eigenschaft des [**Session**](session-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Funktion zurückgibt. Informationen zu Zustands Werten finden Sie unter der Eigenschaft " [**featurerequeststate**](session-featurerequeststate.md) ".

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichen folgen Name der angeforderten Funktion und ein Primärschlüssel in der [Featuretabelle](feature-table.md).

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

[**Featurerequeststate (Eigenschaft)**](session-featurerequeststate.md)
</dt> </dl>

 

 





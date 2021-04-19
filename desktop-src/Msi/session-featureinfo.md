---
description: Die FeatureInfo-Methode des Session-Objekts gibt ein FeatureInfo-Objekt zurück, das beschreibende Informationen für die angegebene Funktion enthält.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Session. FeatureInfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369175"
---
# <a name="sessionfeatureinfo-method"></a>Session. FeatureInfo-Methode

Die **FeatureInfo** -Methode des [**Session**](session-object.md) -Objekts gibt ein **FeatureInfo** -Objekt zurück, das beschreibende Informationen für die angegebene Funktion enthält.

## <a name="syntax"></a>Syntax


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Feature* 
</dt> <dd>

Identifiziert das relevante Feature.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msigetfeatureinfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 





---
description: Die OpenProduct-Methode des Installer-Objekts öffnet ein Installationspaket für ein installiertes Produkt mithilfe des Produktcodes und gibt ein Session-Objekt zurück.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer.OpenProduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129380"
---
# <a name="installeropenproduct-method"></a>Installer.OpenProduct-Methode

Die **OpenProduct-Methode** des [**Installer-Objekts**](installer-object.md) öffnet ein Installationspaket für ein installiertes Produkt mithilfe des Produktcodes und gibt ein [**Session-Objekt**](session-object.md) zurück.

## <a name="syntax"></a>Syntax


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Productcode* 
</dt> <dd>

Erforderliche Zeichenfolge, die den eindeutigen Produktcode [(eine GUID)](guid.md)oder einen vom Installationsprogramm geschriebenen Aktivierungsdeskriptor enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass nur [**ein Sitzungsobjekt**](session-object.md) von einem einzelnen Prozess geöffnet werden kann. **OpenProduct** kann nicht in einer benutzerdefinierten Aktion verwendet werden, da die aktive Installation die einzige zulässige Sitzung ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 





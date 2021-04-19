---
description: Die openproduct-Methode des Installer-Objekts öffnet mithilfe des Produktcodes ein Installationspaket für ein installiertes Produkt und gibt ein Session-Objekt zurück.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer. openproduct-Methode
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
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359765"
---
# <a name="installeropenproduct-method"></a>Installer. openproduct-Methode

Die **openproduct** -Methode des [**Installer**](installer-object.md) -Objekts öffnet mithilfe des Produktcodes ein Installationspaket für ein installiertes Produkt und gibt ein [**Session**](session-object.md) -Objekt zurück.

## <a name="syntax"></a>Syntax


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProductCode* 
</dt> <dd>

Erforderliche Zeichenfolge, die den eindeutigen Produktcode (eine [GUID](guid.md)) oder einen vom Installer geschriebenen Aktivierungs Deskriptor enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass nur ein [**Sitzungs**](session-object.md) Objekt von einem einzelnen Prozess geöffnet werden kann. **Openproduct** kann nicht in einer benutzerdefinierten Aktion verwendet werden, da die aktive Installation die einzige zulässige Sitzung ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





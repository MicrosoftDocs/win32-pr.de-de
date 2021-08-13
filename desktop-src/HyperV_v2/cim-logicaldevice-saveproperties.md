---
description: Fordert an, dass das Gerät die aktuellen Konfigurations-, Einrichtungs- und/oder Zustandsinformationen in einem Hintergrundspeicher erfasst.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: SaveProperties-Methode der CIM_LogicalDevice Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e5910ea87a6321872b009003bf18d26910b53627dba6c51647f2896dde2e686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648162"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>SaveProperties-Methode der CIM \_ LogicalDevice-Klasse

Fordert an, dass das Gerät die aktuellen Konfigurations-, Einrichtungs- und/oder Zustandsinformationen in einem Hintergrundspeicher erfasst. Das Ziel wäre, diese Informationen zu einem späteren Zeitpunkt (über die RestoreProperties-Methode) zu verwenden, um ein Gerät an seine aktuelle "Bedingung" zurückderherzustellen. Diese Methode wird möglicherweise nicht von allen Geräten unterstützt. Die Methode sollte bei Erfolg 0 zurückgeben, 1, wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist. In einer Unterklasse kann der Satz möglicher Rückgabecodes mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. Die Zeichenfolgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 





---
description: Fordert an, dass das Gerät seine aktuellen Konfigurations-, Setup-und/oder Zustandsinformationen in einem Sicherungs Speicher erfasst.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: SaveProperties-Methode der CIM_LogicalDevice-Klasse
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
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373305"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>SaveProperties-Methode der CIM \_ LogicalDevice-Klasse

Fordert an, dass das Gerät seine aktuellen Konfigurations-, Setup-und/oder Zustandsinformationen in einem Sicherungs Speicher erfasst. Das Ziel besteht darin, diese Informationen zu einem späteren Zeitpunkt (über die restoreproperties-Methode) zu verwenden, um ein Gerät an seine vorhandene "Bedingung" zurückzugeben. Diese Methode wird möglicherweise nicht von allen Geräten unterstützt. Die Methode sollte bei erfolgreicher Ausführung 0 (null) zurückgeben, 1, wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist. In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden. Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 





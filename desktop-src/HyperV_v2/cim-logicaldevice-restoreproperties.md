---
description: Fordert an, dass das Gerät seine Konfigurations-, Setup-und/oder Zustandsinformationen aus einem Sicherungs Speicher erneut einrichtet.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Restoreproperties-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362897"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>Restoreproperties-Methode der CIM \_ LogicalDevice-Klasse

Fordert an, dass das Gerät seine Konfigurations-, Setup-und/oder Zustandsinformationen aus einem Sicherungs Speicher erneut einrichtet. Die Absicht besteht darin, diese Informationen zu einem früheren Zeitpunkt (über die SaveProperties-Methode) zu erfassen und damit ein Gerät an diese frühere "Bedingung" zurückzugeben. Diese Methode wird möglicherweise nicht von allen Geräten unterstützt. Die Methode sollte bei erfolgreicher Ausführung 0 (null) zurückgeben, 1, wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist. In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden. Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.

## <a name="syntax"></a>Syntax


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

 

 





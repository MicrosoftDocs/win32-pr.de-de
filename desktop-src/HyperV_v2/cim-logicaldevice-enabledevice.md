---
description: Die enableDevice-Methode wurde anstelle der allgemeineren requestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt, als veraltet markiert.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: EnableDevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362576"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>EnableDevice-Methode der CIM \_ LogicalDevice-Klasse

Die enableDevice-Methode wurde anstelle der allgemeineren requestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt, als veraltet markiert.

Fordert an, dass das LogicalDevice aktiviert ("aktivierter" Eingabeparameter = true) oder deaktiviert (= false) ist. Bei erfolgreicher Ausführung sollte die Status Eigenschaften des Geräts den gewünschten Zustand (aktiviert/deaktiviert) widerspiegeln. Beachten Sie, dass sich die Funktion dieser Methode mit der Eigenschaft requestedstate überlappt. Requestedstate wurde dem Modell hinzugefügt, um einen Datensatz (d. h. einen beibehaltenen Wert) der letzten Zustands Anforderung beizubehalten. Beim Aufrufen der enableDevice-Methode sollte die requestedstate-Eigenschaft entsprechend festgelegt werden.

Der Rückgabecode sollte 0 sein, wenn die Anforderung erfolgreich ausgeführt wurde. der Rückgabecode ist 1, wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist. In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden. Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ in\]
</dt> <dd>

Wenn true, wird das Gerät aktiviert, wenn das Gerät durch false deaktiviert wird.

</dd> </dl>

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

 

 





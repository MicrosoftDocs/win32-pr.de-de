---
description: Die EnableDevice-Methode ist veraltet und nicht mehr die allgemeinere RequestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überschneidet.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: EnableDevice-Methode der CIM_LogicalDevice Klasse
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
ms.openlocfilehash: a01d1b206d0d38f74c5701c8c088506792cb6ca6f997b9e0280adcc61e5a8633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648525"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>EnableDevice-Methode der CIM \_ LogicalDevice-Klasse

Die EnableDevice-Methode ist veraltet und nicht mehr die allgemeinere RequestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überschneidet.

Fordert an, dass LogicalDevice aktiviert ("Enabled" input parameter = TRUE) oder disabled (= FALSE) wird. Bei erfolgreicher Aktivierung sollten die Eigenschaften StatusInfo/EnabledState des Geräts den gewünschten Zustand (aktiviert/deaktiviert) widerspiegeln. Beachten Sie, dass sich die Funktion dieser Methode mit der RequestedState-Eigenschaft überschneidet. RequestedState wurde dem Modell hinzugefügt, um einen Datensatz (d. h. einen persistenten Wert) der letzten Zustandsanforderung zu verwalten. Beim Aufrufen der EnableDevice-Methode sollte die RequestedState-Eigenschaft entsprechend festgelegt werden.

Der Rückgabecode sollte 0 sein, wenn die Anforderung erfolgreich ausgeführt wurde, 1, wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein Fehler aufgetreten ist. In einer Unterklasse kann der Satz möglicher Rückgabecodes mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. Die Zeichenfolgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ In\]
</dt> <dd>

Bei TRUE aktivieren Sie das Gerät, wenn FALSE das Gerät deaktiviert.

</dd> </dl>

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 





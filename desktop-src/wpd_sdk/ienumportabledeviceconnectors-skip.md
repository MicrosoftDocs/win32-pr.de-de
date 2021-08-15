---
description: Überspringt die angegebene Anzahl von Geräten in der Enumerationssequenz.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: IEnumPortableDeviceConnectors::Skip-Methode (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: ba704a2dd232ce5c8ba08d0271e5e0a8fda72f86f9aef89d2e89b04ca9fe94b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546550"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>IEnumPortableDeviceConnectors::Skip-Methode

Die **Skip-Methode** überspringt die angegebene Anzahl von Geräten in der Enumerationssequenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cConnectors* \[ In\]
</dt> <dd>

Die Anzahl der zu überspringenden Geräte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die angegebene Anzahl von Geräten konnte nicht übersprungen werden. Eine mögliche Ursache: Der *cConnectors-Parameter* gibt mehr Geräte an, als tatsächlich in der Enumerationssequenz verbleiben.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                   |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 





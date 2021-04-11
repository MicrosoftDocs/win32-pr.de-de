---
description: Überspringt die angegebene Anzahl von Geräten in der enumerationssequenz.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Ienumportabledeviceconnectors:: Skip-Methode (devpkey. h)'
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
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042618"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>Ienumportabledeviceconnectors:: Skip-Methode

Die **Skip** -Methode überspringt die angegebene Anzahl von Geräten in der enumerationssequenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cconnectors* \[ in\]
</dt> <dd>

Die Anzahl der zu über springenden Geräte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                                                                          |
| <dl> <dt>**S \_ false**</dt> </dl> | Die angegebene Anzahl von Geräten konnte nicht übersprungen werden. Eine mögliche Ursache: der *cconnectors* -Parameter gibt mehr Geräte an, als Sie tatsächlich in der enumerationssequenz verbleiben.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                   |
| Header<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portablede viceconnectapi. idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>Portabledeviceguids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumportablede viceconnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 





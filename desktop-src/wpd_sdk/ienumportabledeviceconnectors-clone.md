---
description: Erstellt eine Kopie der aktuellen ienumportabledebug Controller-Schnittstelle.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Ienumportabledeviceconnectors:: Clone-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348568"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a>Ienumportabledeviceconnectors:: Clone-Methode

Die **Clone** -Methode erstellt eine Kopie der aktuellen [**ienumportabledeviceconnectors**](ienumportabledeviceconnectors.md) -Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Zeigers auf eine [**ienumportabledebug Controller**](ienumportabledeviceconnectors.md) -Schnittstelle. Diese Schnittstelle muss von der aufrufenden Anwendung freigegeben werden, wenn Sie damit abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portablede viceconnectapi. idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>Portabledeviceguids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumportablede viceconnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 





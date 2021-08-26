---
description: Erstellt eine Kopie der aktuellen IEnumPortableDeviceConnectors-Schnittstelle.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: IEnumPortableDeviceConnectors::Clone-Methode (Devpkey.h)
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
ms.openlocfilehash: 53b9c49b5bf36571409cd49026d5d08fced80c3e43aee63d844abd481e51aa3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055330"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a>IEnumPortableDeviceConnectors::Clone-Methode

Die **Clone-Methode** erstellt eine Kopie der aktuellen [**IEnumPortableDeviceConnectors-Schnittstelle.**](ienumportabledeviceconnectors.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Die Adresse eines Zeigers auf eine [**IEnumPortableDeviceConnectors-Schnittstelle.**](ienumportabledeviceconnectors.md) Die aufrufende Anwendung muss diese Schnittstelle wieder frei geben, wenn sie damit fertig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 





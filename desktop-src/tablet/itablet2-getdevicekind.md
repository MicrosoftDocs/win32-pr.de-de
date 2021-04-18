---
description: Gibt den Typ des Hardware Geräts zurück, das das Tablet-Objekt darstellt, z. b. Maus, Stift oder Fingereingabe
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'ITablet2:: getdevicekind-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359130"
---
# <a name="itablet2getdevicekind-method"></a>ITablet2:: getdevicekind-Methode

Gibt den Typ des Hardware Geräts zurück, das das Tablet-Objekt darstellt, z. b. Maus, Stift oder Fingereingabe

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pkind* \[ vorgenommen\]
</dt> <dd>

-Enumerationswert, der den Typ des Tablets angibt, z. b. Maus, Stift oder Fingereingabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle und Methode wurden in Windows Vista eingeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet2-Schnittstelle**](itablet2.md)
</dt> <dt>

[**Tablet \_ Device \_ Kind-Enumeration**](tablet-device-kind.md)
</dt> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> </dl>

 

 





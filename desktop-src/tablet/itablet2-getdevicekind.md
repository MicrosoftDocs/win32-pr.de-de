---
description: Gibt den Typ des Hardwaregeräts zurück, das das Tablettobjekt darstellt, z. B. Maus, Stift oder Fingereingabe.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: ITablet2::GetDeviceKind-Methode
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
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450527"
---
# <a name="itablet2getdevicekind-method"></a>ITablet2::GetDeviceKind-Methode

Gibt den Typ des Hardwaregeräts zurück, das das Tablettobjekt darstellt, z. B. Maus, Stift oder Fingereingabe.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pKind* \[ out\]
</dt> <dd>

Enumerationswert, der den Tabletttyp angibt, z. B. Maus, Stift oder Fingereingabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle und Methode wurden in Windows Vista eingeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**ITablet2-Schnittstelle**](itablet2.md)
</dt> <dt>

[**TABLET \_ DEVICE \_ KIND-Enumeration**](tablet-device-kind.md)
</dt> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> </dl>

 

 





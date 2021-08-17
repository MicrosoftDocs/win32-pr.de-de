---
description: Aktualisiert den Tablettdigitalisierer in Fensterpositionszuordnungskoordinaten.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: ITabletContextP::TrackInputRect-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 400055247583ec0bd2095d5d6f68d8481c69fd6bb4e7f7730344120203655ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350570"
---
# <a name="itabletcontextptrackinputrect-method"></a>ITabletContextP::TrackInputRect-Methode

Aktualisiert den Tablettdigitalisierer in Fensterpositionszuordnungskoordinaten.

## <a name="syntax"></a>Syntax


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prcInput* \[ out\]
</dt> <dd>

Das neue Eingabefensterrechteck, nachdem die Zuordnung zwischen den Fenster- und Digitizerkoordinaten aktualisiert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode jederzeit auf, wenn sich die Position des Fensters auf dem Bildschirm ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletContextP-Schnittstelle**](itabletcontextp.md)
</dt> </dl>

 

 





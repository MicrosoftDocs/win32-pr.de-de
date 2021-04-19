---
description: Aktualisiert den Tablet-Digitalisierer auf Fenster Speicherort-Mapping-Koordinaten.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'Itabletcontextp:: trackinputrect-Methode'
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
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353945"
---
# <a name="itabletcontextptrackinputrect-method"></a>Itabletcontextp:: trackinputrect-Methode

Aktualisiert den Tablet-Digitalisierer auf Fenster Speicherort-Mapping-Koordinaten.

## <a name="syntax"></a>Syntax


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prcinput* \[ vorgenommen\]
</dt> <dd>

Das neue Eingabefenster Rechteck nach dem Aktualisieren der Zuordnung zwischen der Fenster-und der Digitalisierungs Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Position des Fensters auf dem Bildschirm geändert wird, wird diese Methode aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletcontextp-Schnittstelle**](itabletcontextp.md)
</dt> </dl>

 

 





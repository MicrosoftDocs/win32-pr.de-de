---
description: Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'Itabletcursor:: getbuttoncount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363733"
---
# <a name="itabletcursorgetbuttoncount-method"></a>Itabletcursor:: getbuttoncount-Methode

Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcbuttons* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Schaltflächen auf dem Tablettstift.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletcursor-Schnittstelle**](itabletcursor.md)
</dt> </dl>

 

 





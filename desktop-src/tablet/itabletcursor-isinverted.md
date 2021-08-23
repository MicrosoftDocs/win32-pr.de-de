---
description: Gibt an, ob der Stift auf dem Kopf steht.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: ITabletCursor::IsInverted-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 81bbb5f4f93026e0d6910cb7f23d0a7d2ddeea5595e87f816faa016d22986d0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223068"
---
# <a name="itabletcursorisinverted-method"></a>ITabletCursor::IsInverted-Methode

Gibt an, ob der Stift auf dem Kopf steht.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                             | Beschreibung                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Stift ist invertiert.<br/>        |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Stift ist nicht invertiert.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**ITabletCursorButton-Schnittstelle**](itabletcursorbutton.md)
</dt> </dl>

 

 





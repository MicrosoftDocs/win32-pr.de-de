---
description: Gibt an, ob der Tablettstift aufwärts unten ist.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Itabletcursor:: isinvertierte-Methode'
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
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364072"
---
# <a name="itabletcursorisinverted-method"></a>Itabletcursor:: isinvertierte-Methode

Gibt an, ob der Tablettstift aufwärts unten ist.

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
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Tablettstift ist invertiert.<br/>        |
| <dl> <dt>**S \_ false**</dt> </dl> | Der Tablettstift wird nicht invertiert.<br/>    |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>  | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletcursor**](itabletcursor.md)
</dt> <dt>

[**Itabletcursor Button-Schnittstelle**](itabletcursorbutton.md)
</dt> </dl>

 

 





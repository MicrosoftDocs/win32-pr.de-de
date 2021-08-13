---
description: Gibt an, ob sich der Tablet-Kontext im obersten Hook befindet.
ms.assetid: b4aaee47-3d77-49cd-9600-f41764b9fb85
title: ITabletContextP::IsTopMostHook-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.IsTopMostHook
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 1c7b7e1fa087dad42e7bdc3b803bd7158b8859d1d428714f6eb2c4321687a603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449803"
---
# <a name="itabletcontextpistopmosthook-method"></a>ITabletContextP::IsTopMostHook-Methode

Gibt an, ob sich der Tablet-Kontext im obersten Hook befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsTopMostHook();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**ITabletContextP-Schnittstelle**](itabletcontextp.md)
</dt> </dl>

 

 





---
title: ISoftKbd ShowSoftKeyboard-Methode (Softkbdc.h)
description: Die ShowSoftKeyboard-Methode ISoftKbd zeigt eine soft-Tastatur an.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- ShowSoftKeyboard-Methode Textdienstframework
- ShowSoftKeyboard-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , ShowSoftKeyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cd0e7addcbb58f1cf383d59a5536b3e0737df2dee189bc728fd3084fd35f34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952425"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a>ISoftKbd::ShowSoftKeyboard-Methode

Die **ISoftKbd::ShowSoftKeyboard-Methode** zeigt eine soft-Tastatur an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iShow* \[ In\]
</dt> <dd>

Ganze Zahl, die den Typ der anzuzeigende Softtastatur angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                | Beschreibung                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 






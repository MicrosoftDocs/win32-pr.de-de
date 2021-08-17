---
description: Ruft den Namen der Stiftschaltfläche ab.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: ITabletCursorButton::GetName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 41155aa15a2efaeb789387ae3ea7c6863ab0010884ecacb2f7bd3a75453e57b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716820"
---
# <a name="itabletcursorbuttongetname-method"></a>ITabletCursorButton::GetName-Methode

Ruft den Namen der Stiftschaltfläche ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppwszName* \[ out\]
</dt> <dd>

Der Name der Tablettstiftschaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Aufrufer ist dafür verantwortlich, den von dieser Methode zurückgegebenen Arbeitsspeicher mithilfe von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletCursorButton-Schnittstelle**](itabletcursorbutton.md)
</dt> </dl>

 


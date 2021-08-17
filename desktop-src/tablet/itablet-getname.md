---
description: Gibt eine Zeichenfolge zurück, die den Namen des Tablettgeräts enthält.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: ITablet::GetName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 089bebc48fce9c720933f829ab83d04bf24fac3d8e2678369865cf2fe58650f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350679"
---
# <a name="itabletgetname-method"></a>ITablet::GetName-Methode

Gibt eine Zeichenfolge zurück, die den Namen des Tablettgeräts enthält.

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

Zeiger auf eine Zeichenfolge, die den Namen des Tablettgeräts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Es liegt in der Verantwortung des Aufrufers, den von dieser Methode zurückgegebenen Arbeitsspeicher mithilfe von [**CoTaskMemFree frei zu geben.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> </dl>

 


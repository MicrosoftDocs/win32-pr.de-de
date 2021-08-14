---
title: FreeUiInfo-Funktion (Ndattributils.h)
description: Gibt die interne Speicherbelegung für eine UiInfo-Struktur auf.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo-Funktion NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e2008ddabdb412c117a3cfac5f2eb5ebf1e722f5f3729fb7c8b2ee0c394c454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939047"
---
# <a name="freeuiinfo-function"></a>FreeUiInfo-Funktion

Die **FreeUiInfo-Funktion** gibt den internen Speicher frei, der einer [**UiInfo-Struktur zugeordnet**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) ist. Diese Funktion ruft [**CoTaskMemFree auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um die Speicherverteilung frei zu machen.

## <a name="syntax"></a>Syntax


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInfo* \[ In\]
</dt> <dd>

Typ: **[ **UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\***

Die -Struktur. Der zugeordnete Arbeitsspeicher, auf den diese Struktur zeigt, wird frei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


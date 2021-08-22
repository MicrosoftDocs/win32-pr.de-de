---
description: Ruft die Standardkontexteinstellungen für das Tablet ab.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: ITablet::GetDefaultContextSettings-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 646756a924bd9b848f2141b796205f2cf2374140811b7dd87f8ffd64c69ee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336260"
---
# <a name="itabletgetdefaultcontextsettings-method"></a>ITablet::GetDefaultContextSettings-Methode

Ruft die Standardkontexteinstellungen für das Tablet ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppTCS* \[ out\]
</dt> <dd>

Die Standardkontexteinstellungen für das Tablet.

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

 


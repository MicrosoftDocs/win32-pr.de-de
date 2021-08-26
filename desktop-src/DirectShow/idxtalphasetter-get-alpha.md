---
description: Die \_ Methode get Alpha ruft den Alphawert für das gesamte Bild ab.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: IDxtAlphaSetter::get_Alpha-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 054e2a1745f96dc4d6ea846bed0448948fae8407dd6ab44d2796742e405f2e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051970"
---
# <a name="idxtalphasetterget_alpha-method"></a>IDxtAlphaSetter::get \_ Alpha-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_Alpha` -Methode ruft den Alphawert für das gesamte Bild ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Empfängt den Alphawert. Dieser Alphawert wird auf das gesamte Zielbild angewendet. Ein negativer Wert gibt an, dass kein Alphawert festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                               | Beschreibung                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerargument**<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                   |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDxtAlphaSetter-Schnittstelle**](idxtalphasetter.md)
</dt> </dl>

 

 





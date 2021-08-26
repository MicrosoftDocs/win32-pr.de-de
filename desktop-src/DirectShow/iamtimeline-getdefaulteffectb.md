---
description: Die GetDefaultEffectB-Methode ruft den Standardeffekt ab. Diese Methode entspricht IAMTimeline::GetDefaultEffect, empfängt jedoch einen BSTR-Wert anstelle einer GUID.
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: IAMTimeline::GetDefaultEffectB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f0abfac297817b4e93b4eabe5bd2517c22ab363498bbbe35f2b5ae449524ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997770"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>IAMTimeline::GetDefaultEffectB-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetDefaultEffectB` -Methode ruft den Standardeffekt ab. Diese Methode entspricht [**IAMTimeline::GetDefaultEffect,**](iamtimeline-getdefaulteffect.md)empfängt jedoch einen **BSTR-Wert** anstelle einer GUID.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Empfängt einen **BSTR-Wert,** der die GUID des Standardeffekts darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die -Methode ordnet Arbeitsspeicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString aufrufen,** um den Arbeitsspeicher frei zu machen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





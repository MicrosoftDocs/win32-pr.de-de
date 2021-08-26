---
description: Die GetDefaultTransitionB-Methode ruft den Standardübergang ab. Diese Methode entspricht IAMTimeline::GetDefaultTransition, empfängt jedoch einen BSTR-Wert anstelle einer GUID.
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: IAMTimeline::GetDefaultTransitionB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 39725fc4e4f5c9f02dcd092fddba632262c3b8a0aa85e27afd7df1afb9bb314c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107840"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a>IAMTimeline::GetDefaultTransitionB-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetDefaultTransitionB` -Methode ruft den Standardübergang ab. Diese Methode entspricht [**IAMTimeline::GetDefaultTransition,**](iamtimeline-getdefaulttransition.md)empfängt jedoch einen BSTR-Wert anstelle einer GUID.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Empfängt einen **BSTR-Wert,** der die GUID des Standardübergangs darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die -Methode belegt Arbeitsspeicher für die Zeichenfolge. Die Anwendung muss **SysFreeString** aufrufen, um den Arbeitsspeicher freizugeben.

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

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





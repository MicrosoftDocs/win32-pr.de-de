---
description: Die \_ get AlphaRamp-Methode ruft die Alphaverlaufseigenschaft ab. Die Alpha-Rampe ist der Prozentsatz, um den die Alphawerte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe beispielsweise 0,5 ist, werden die Alphawerte im Bild um 50 % reduziert.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: IDxtAlphaSetter::get_AlphaRamp-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9768ed96f0b40e074fd44de04ca44a8cc17d9de7ce4b75af948975e26b5e3077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952739"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>IDxtAlphaSetter::get \_ AlphaRamp-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_AlphaRamp` -Methode ruft die Alpha-Rampeneigenschaft ab. Die Alpha-Rampe ist der Prozentsatz, um den die Alphawerte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe beispielsweise 0,5 ist, werden die Alphawerte im Bild um 50 % reduziert.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Empfängt die Alpha-Rampe. Ein negativer Wert gibt an, dass keine Alpha-Rampe festgelegt ist.

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

 

 





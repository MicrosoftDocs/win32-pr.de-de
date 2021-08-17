---
description: Die \_ put AlphaRamp-Methode gibt die Alphaverlaufseigenschaft an. Die Alpha-Rampe ist der Prozentsatz, um den die Alphawerte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe beispielsweise 0,5 ist, werden die Alphawerte im Bild um 50 % reduziert.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: IDxtAlphaSetter::p ut_AlphaRamp-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88661c40ea0824d643909f688a7d86251c434e0e3dcc88d8a3aec97dcb6b40c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952729"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>IDxtAlphaSetter::p ut \_ AlphaRamp-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `put_AlphaRamp` -Methode gibt die Alphaverlaufseigenschaft an. Die Alpha-Rampe ist der Prozentsatz, um den die Alphawerte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe beispielsweise 0,5 ist, werden die Alphawerte im Bild um 50 % reduziert.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Alpha* \[ In\]
</dt> <dd>

Die Alpha-Rampe als Prozentsatz. Beispielsweise ist 1,0 100 %. Um diese Eigenschaft zu deaktivieren, legen Sie einen negativen Wert fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn Sie diese Eigenschaft auf einen nicht negativen Wert festlegen, müssen Sie auch die Alphaeigenschaft deaktivieren, indem Sie **put \_ Alpha** mit einem negativen Wert aufrufen. Andernfalls wird der Effekt nicht ordnungsgemäß gerendert.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDxtAlphaSetter-Schnittstelle**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::put \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 





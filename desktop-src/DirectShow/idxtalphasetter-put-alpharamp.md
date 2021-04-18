---
description: Die Put \_ alpharamp-Methode gibt die Eigenschaft für die Alpha-Eigenschaft an. Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: Idxtalphasetter::p ut_AlphaRamp-Methode (qedit. h)
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
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371791"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>Idxtalphasetter::p UT \_ alpharamp-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_AlphaRamp` Methode gibt die Eigenschaft der Alpha-Eigenschaft an. Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Alpha* \[ in\]
</dt> <dd>

Die Alpha-Rampe als Prozentsatz. 1,0 ist beispielsweise 100%. Legen Sie zum Deaktivieren dieser Eigenschaft einen negativen Wert fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Eigenschaft auf einen nicht negativen Wert festlegen, müssen Sie auch die Alpha-Eigenschaft deaktivieren, indem Sie **Put \_ Alpha** mit einem negativen Wert aufrufen. Andernfalls wird der Effekt nicht korrekt dargestellt.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idxtalphasetter-Schnittstelle**](idxtalphasetter.md)
</dt> <dt>

[**Idxtalphasetter::p UT \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 





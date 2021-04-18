---
description: Die Put \_ Alpha-Methode gibt den Alpha-Wert für das gesamte Bild an.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: Idxtalphasetter::p ut_Alpha-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372133"
---
# <a name="idxtalphasetterput_alpha-method"></a>Idxtalphasetter::p UT \_ Alpha-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_Alpha` Methode gibt den Alpha-Wert für das gesamte Bild an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Alpha* \[ in\]
</dt> <dd>

Der Alphawert. Dieser Wert wird auf das gesamte Zielbild angewendet. Legen Sie zum Deaktivieren dieser Eigenschaft einen negativen Wert fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Eigenschaft auf einen nicht negativen Wert festlegen, müssen Sie auch die Eigenschaft Alpha-Rampe deaktivieren, indem Sie **Put \_ alpharamp** mit einem negativen Wert aufrufen. Andernfalls wird der Effekt nicht korrekt dargestellt.

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

[**Idxtalphasetter::p UT \_ alpharamp**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 





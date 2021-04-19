---
description: Die Put \_ Width-Methode gibt die Breite des Ziel Rechtecks an.
ms.assetid: 16a2d860-6f5d-4f36-ba54-1be2d3fef705
title: Idxtcompositor::p ut_Width-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Width
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 55cc3f2f97be2176f13ce3655d3844ef94043409
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367728"
---
# <a name="idxtcompositorput_width-method"></a>Idxtcompositor::p UT \_ Width-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_Width` Methode gibt die Breite des Ziel Rechtecks an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Width(
  [in] long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Die Breite des Ziel Rechtecks in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

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

[**Idxtcompositor-Schnittstelle**](idxtcompositor.md)
</dt> </dl>

 

 





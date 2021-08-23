---
description: Die methode get \_ MaskName ruft den Namen einer JPEG-Datei ab, die als Zurücksetzungsmaske verwendet werden soll.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: IDxtJpeg::get_MaskName-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d984f426289b9017ca316567b474beaa41b39a35f0ab012ea94ffdd8db33a36b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584740"
---
# <a name="idxtjpegget_maskname-method"></a>IDxtJpeg::get \_ MaskName-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_MaskName` -Methode ruft den Namen einer JPEG-Datei ab, die als Zurücksetzungsmaske verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt den Dateinamen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der Zurücksetzungsübergang eines der integrierten SMPTE-Zurücksetzungen verwendet, die er unterstützt, ist der Wert dieser Eigenschaft eine leere Zeichenfolge.

Der Aufrufer muss die zurückgegebene Zeichenfolge mithilfe der **SysFreeString-Funktion** veröffentlichen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDxtJpeg-Schnittstelle**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg::get \_ MaskNum**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 





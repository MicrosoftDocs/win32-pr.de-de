---
description: Die Put \_ masknum-Methode gibt den SMPTE-Code zum Löschen der Löschung an.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: Idxtjpeg::p ut_MaskNum-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356439"
---
# <a name="idxtjpegput_masknum-method"></a>Idxtjpeg::p UT \_ masknum-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_MaskNum` Methode gibt den SMPTE-Code zum Löschen der Löschung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Gibt den SMPTE-Code zum Löschen an. Eine Liste der unterstützten SMPTE-Wipes finden Sie unter [SMPTE](smpte-wipe-transition.md)-Zurücksetzungs Übergang.

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

[**Idxtjpeg-Schnittstelle**](idxtjpeg.md)
</dt> </dl>

 

 





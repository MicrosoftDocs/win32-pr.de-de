---
description: Die Put \_ maskname-Methode gibt den Namen einer JPEG-Datei an, die als abzurufende Maske verwendet werden soll.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: Idxtjpeg::p ut_MaskName-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367081"
---
# <a name="idxtjpegput_maskname-method"></a>Idxtjpeg::p UT \_ maskname-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_MaskName` Methode gibt den Namen einer JPEG-Datei an, die als abzurufende Maske verwendet werden soll. Diese Maske wird anstelle einer der integrierten Masken für das Löschen verwendet. Die Datei muss einen Farbverlauf von 8 Bits pro Pixel enthalten. Der Farbverlauf wird als Maske zum Definieren des Fortschritts der Löschung verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Gibt den Namen der Datei an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Legen Sie die **masknum** -Eigenschaft fest, um zu einer integrierten Maske zurückzukehren.

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
</dt> <dt>

[**Idxtjpeg::p UT- \_ masknum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 





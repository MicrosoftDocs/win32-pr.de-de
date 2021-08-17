---
description: Die SetMediaName-Methode gibt den Namen der Quelldatei an, die durch dieses Quellobjekt dargestellt wird.
ms.assetid: 60307c87-9dce-4e60-b14b-07d2c8604dd8
title: IAMTimelineSrc::SetMediaName-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 99a4856b8d0a566b0b86338019c5a455e5e6fca9a521d19d2b92b3bc5dcdc4c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399217"
---
# <a name="iamtimelinesrcsetmedianame-method"></a>IAMTimelineSrc::SetMediaName-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetMediaName` -Methode gibt den Namen der Quelldatei an, die durch dieses Quellobjekt dargestellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaName(
   BSTR newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* 
</dt> <dd>

Eine Zeichenfolge, die den Namen der Mediendatei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





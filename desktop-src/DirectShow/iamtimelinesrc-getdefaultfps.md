---
description: Die getdefaultfps-Methode ruft die Standardbildrate des Quell Objekts ab. Die Renderingengine verwendet diesen Wert, wenn Sie die Framerate aus der ursprünglichen Quelle nicht ermitteln kann.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Iamtimelinesrc:: getdefaultfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367519"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>Iamtimelinesrc:: getdefaultfps-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetDefaultFPS` -Methode ruft die Standardbildrate des Quell Objekts ab. Die Renderingengine verwendet diesen Wert, wenn Sie die Framerate aus der ursprünglichen Quelle nicht ermitteln kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfps* 
</dt> <dd>

Empfängt die Standardbildrate in Frames pro Sekunde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Standardbildrate ist nicht erforderlich, wenn das Dateiformat die Framerate angibt. Dies ist der Fall bei Audio-und Videoformaten.

Wenn es sich bei der Quelle um ein Bitmap-oder JPEG-Bild handelt, verwendet die Renderingengine Sie als erstes Bild in einer geräteunabhängigen Bitmap-Sequenz (DIB) mit einer Frame Rate, die der Standard Frame Rate entspricht. Wenn Sie ein statisches Bild anstelle einer DIB-Sequenz darstellen möchten, legen Sie die Standardbildrate auf 0 fest.

Wenn die Quelle eine GIF ist, legen Sie die Framerate nicht fest. Bei animierten GIFs gibt die GIF-Datei die Verzögerung zwischen jedem Bild an.

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





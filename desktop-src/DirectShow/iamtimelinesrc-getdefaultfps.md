---
description: Die GetDefaultFPS-Methode ruft die Standardbildfrequenz des Quellobjekts ab. Die Render-Engine verwendet diesen Wert, wenn sie die Bildfrequenz aus der ursprünglichen Quelle nicht bestimmen kann.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: IAMTimelineSrc::GetDefaultFPS-Methode (Qedit.h)
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
ms.openlocfilehash: 92154a4c97c46307a764a7dba22ff2e003621db59cdb962ff025635022a5384b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131210"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>IAMTimelineSrc::GetDefaultFPS-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetDefaultFPS` -Methode ruft die Standardbildfrequenz des Quellobjekts ab. Die Render-Engine verwendet diesen Wert, wenn sie die Bildfrequenz aus der ursprünglichen Quelle nicht bestimmen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfps* 
</dt> <dd>

Empfängt die Standardbildfrequenz in Frames pro Sekunde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Standardbildfrequenz ist nicht erforderlich, wenn das Dateiformat die Bildfrequenz angibt. Dies ist bei Audio- und Videoformaten der Fall.

Wenn es sich bei der Quelle um ein Bitmap- oder JPEG-Bild handelt, verwendet die Render-Engine es als erstes Bild in einer geräteunabhängigen Bitmapsequenz (DIB) mit einer Bildfrequenz, die der Standardbildfrequenz entspricht. Legen Sie zum Rendern eines statischen Bilds anstelle einer DIB-Sequenz die Standardbildrate auf 0 fest.

Wenn es sich bei der Quelle um ein GIF handelt, legen Sie die Bildfrequenz nicht fest. Bei animierten GIFs gibt die GIF-Datei die Verzögerung zwischen den einzelnen Bildern an.

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





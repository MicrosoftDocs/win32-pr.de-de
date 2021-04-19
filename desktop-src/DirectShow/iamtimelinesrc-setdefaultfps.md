---
description: Die setdefaultfps-Methode legt die Standard Frame Rate des Quell Objekts fest.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Iamtimelinesrc:: setdefaultfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362007"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>Iamtimelinesrc:: setdefaultfps-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetDefaultFPS` -Methode legt die Standardbildrate des Quell Objekts fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FPS* 
</dt> <dd>

Standard Frame Rate in Frames pro Sekunde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder E \_ invalidArg zurück, wenn die angegebene Framerate kleiner als 0 (null) ist.

## <a name="remarks"></a>Bemerkungen

Die Renderingengine verwendet diesen Wert, wenn Sie die Framerate der ursprünglichen Quelldatei nicht ermitteln kann.

Diese Methode wird nur für Quelldateien ohne vordefinierte Framerate aufgerufen. Bei Bitmap-und JPEG-Dateien ist die Standardbildrate NULL. Dadurch wird die Quelle als Bild gerendert. Um das Bild als ersten Frame in einer DIB-Sequenz zu verwenden, legen Sie die Framerate auf einen Wert größer als 0 (null) fest. Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md).

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

 

 





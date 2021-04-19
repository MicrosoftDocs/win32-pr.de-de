---
description: Die Methode "*-martrecompressformat" gibt ein Video Komprimierungs Format an, das für die intelligente Neukomprimierung verwendet wird.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: Iamtimelinegroup::-Methode für das-martrecompressformat (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361424"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>Iamtimelinegroup::.

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetSmartRecompressFormat` Methode gibt ein Video Komprimierungs Format an, das für die intelligente Neukomprimierung verwendet wird.

Die intelligente Neukomprimierung wird für Audiogruppen nicht unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Zeiger auf eine-Struktur, die das Komprimierungs Format beschreibt. Derzeit ist nur die [**SCompFmt0**](scompfmt0.md) -Struktur gültig. Sie müssen diesen Parameter in einen Zeiger vom Typ **Long** umwandeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Methode aufrufen, rufen Sie die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode für die gleiche Gruppe auf, um ein nicht komprimiertes Format anzugeben.

Wenn die `SetSmartRecompressFormat` Methode erfolgreich ist, können Sie die Smart-Rendering-Engine zum Ausgeben eines komprimierten Videodaten Stroms verwenden. Das komprimierte Video enthält die Breite, Höhe und Framerate, die im *pformat* -Parameter angegeben wurde. Diese Werte überschreiben die Werte, die für das unkomprimierte Format in der **setmediatype** -Methode angegeben werden. Um jedoch die Vorteile der intelligenten Neukomprimierung zu erzielen, sollten die beiden Formate identisch sein. Das heißt, die komprimierten und unkomprimierten Formate sollten die gleiche Höhe, Breite und Framerate aufweisen.

Wenn die Smart-Rendering-Engine das komprimierte Format nicht erzeugen kann, wird stattdessen ein unkomprimierter Videostream erzeugt. Wenn dies der Fall ist, meldet das Smart-Rendering-Modul \_ \_ \_ \_ bei der Methode " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md) " eine DEX-ID nicht. Die Anwendung kann diesen Fehler durch die [**iamerrorlog:: LogError**](iamerrorlog-logerror.md) -Methode abfangen. (Weitere Informationen finden Sie unter [Protokollieren von Fehlern](logging-errors.md) und [Rendern von Fehlern](rendering-errors.md).)

Das Format der intelligenten Neukomprimierung ist nicht persistent. Wenn eine Anwendung eine intelligente Neukomprimierung verwendet, muss Sie beim Laden einer Projektdatei das neukomprimierungs Format festlegen.

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

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[Smart-Rendering-Engine](smart-render-engine.md)
</dt> <dt>

[Schreiben eines Projekts in eine Datei](writing-a-project-to-a-file.md)
</dt> </dl>

 

 





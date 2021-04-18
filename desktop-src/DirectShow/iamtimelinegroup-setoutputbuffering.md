---
description: Die setoutputbuffereing-Methode gibt die Anzahl der Rahmen an, die während der Vorschau vorab gerendert werden.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Iamtimelinegroup:: setoutputbuffereing-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371706"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>Iamtimelinegroup:: setoutputbuffereing-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetOutputBuffering` Methode gibt die Anzahl der Rahmen an, die während der Vorschau vorab gerendert werden

## <a name="syntax"></a>Syntax


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*npuffer* \[ in\]
</dt> <dd>

Anzahl der Rahmen, die während der Vorschau puffert werden. Muss zwei oder größer sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein größerer Puffer benötigt mehr Arbeitsspeicher, kann jedoch zu einer glatteren Vorschau der Anzeige führen, insbesondere bei Effekten oder Übergängen, die mehr Zeit für das Rendering benötigen. Der Standard Puffer ist 30 Frames.

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
</dt> </dl>

 

 





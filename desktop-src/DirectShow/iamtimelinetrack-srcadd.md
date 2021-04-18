---
description: Die srcadd-Methode fügt der Spur eine Quelle hinzu.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Iamtimelinetrack:: srcadd-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357565"
---
# <a name="iamtimelinetracksrcadd-method"></a>Iamtimelinetrack:: srcadd-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SrcAdd` Methode fügt der Spur eine Quelle hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrc* 
</dt> <dd>

Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Gibt "E nointerface" zurück, \_ Wenn das Objekt kein Quell Objekt ist. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Legen Sie die Start-und Endzeiten der Quelle vor dem Aufrufen dieser Methode fest. (Aufrufen von [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md).)

Derzeit kann des nicht gleichzeitig mehr als 75 Quellen gleichzeitig erzeugen, die mit Video Compression Manager-Codecs (VCM) komprimiert wurden. Wenn das Projekt als Ganzes mehr als 75 derartige Quellen enthält, müssen Sie auch die dynamische Neuverbindung verwenden, oder des kann das Projekt nicht in der Vorschau anzeigen. Weitere Informationen finden Sie unter " [**unenderengine:: setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)".

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

[**Iamtimelinetrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





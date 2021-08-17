---
description: Die SrcAdd-Methode fügt der Spur eine Quelle hinzu.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: IAMTimelineTrack::SrcAdd-Methode (Qedit.h)
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
ms.openlocfilehash: e705f840a073ee6796776f6f68c7b57df0bd972facf8f7a586792519735bfb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998750"
---
# <a name="iamtimelinetracksrcadd-method"></a>IAMTimelineTrack::SrcAdd-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SrcAdd` -Methode fügt der Spur eine Quelle hinzu.

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

Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Quellobjekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich. Gibt E \_ NOINTERFACE zurück, wenn das -Objekt kein Quellobjekt ist. Andernfalls gibt einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Legen Sie die Start- und Stoppzeiten der Quelle fest, bevor Sie diese Methode aufrufen. (Rufen Sie [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)auf.)

Derzeit kann DES nicht mehr als 75 Quellen gleichzeitig rendern, die mit VCM-Codecs (Video Compression Manager) komprimiert wurden. Wenn das Projekt als Ganzes mehr als 75 solcher Quellen enthält, müssen Sie die dynamische Wiederherstellungsverbindung verwenden, oder DES kann keine Vorschau des Projekts anzeigen. Weitere Informationen finden Sie unter [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





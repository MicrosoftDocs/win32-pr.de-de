---
description: Wird nicht unterstützt. Rufen Sie die IAMTimeline::CreateEmptyNode-Methode auf, um ein neues Zeitachsenobjekt zu erstellen. Nachdem ein Objekt erstellt wurde, können Sie seinen Typ nicht mehr ändern.
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: IAMTimelineObj::SetTimelineType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4592c92c4c40f9fff8294ea546601654afd0111e38fd9f64473512c27b6f1a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400851"
---
# <a name="iamtimelineobjsettimelinetype-method"></a>IAMTimelineObj::SetTimelineType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Wird nicht unterstützt. Rufen Sie die [**IAMTimeline::CreateEmptyNode-Methode**](iamtimeline-createemptynode.md) auf, um ein neues Zeitachsenobjekt zu erstellen. Nachdem ein Objekt erstellt wurde, können Sie seinen Typ nicht mehr ändern.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* 
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> </dl>

 

 





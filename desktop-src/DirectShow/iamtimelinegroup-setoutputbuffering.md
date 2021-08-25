---
description: Die SetOutputBuffering-Methode gibt die Anzahl der Frames an, die während der Vorschau im Voraus gerendert wurden.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: IAMTimelineGroup::SetOutputBuffering-Methode (Qedit.h)
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
ms.openlocfilehash: 8187918a4f6d04df9c8c0eaff387a092f18181071ce6ba41c83de44fcb095bbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915190"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>IAMTimelineGroup::SetOutputBuffering-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetOutputBuffering` -Methode gibt die Anzahl der Frames an, die während der Vorschau im Voraus gerendert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nBuffer* \[ In\]
</dt> <dd>

Anzahl der Frames, die während der Vorschau gepuffert werden sollen. Muss zwei oder größer sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Ein größerer Puffer erfordert mehr Arbeitsspeicher, kann aber zu einer reibungsloseren Vorschau führen, insbesondere bei Effekten oder Übergängen, die mehr Zeit für das Rendern benötigen. Der Standardpuffer ist 30 Frames.

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

[**IAMTimelineGroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





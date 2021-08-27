---
description: Die GetTimeline-Methode ruft die Zeitachse ab, zu der diese Gruppe gehört.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: IAMTimelineGroup::GetTimeline-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: da9064969cc026ebffb91ccbdb70bcaebab2b5d696bcb04d6c6281548721c522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086840"
---
# <a name="iamtimelinegroupgettimeline-method"></a>IAMTimelineGroup::GetTimeline-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetTimeline` -Methode ruft die Zeitachse ab, zu der diese Gruppe gehört.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppTimeline* \[ out\]
</dt> <dd>

Empfängt die [**IAMTimeline-Schnittstelle**](iamtimeline.md) der Zeitachse. Wenn die Gruppe nicht Teil einer Zeitachse ist, wird der Wert auf **NULL** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der in *ppTimeline* zurückgegebene Wert nicht **NULL** ist, verfügt die **IAMTimeline-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

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

 

 





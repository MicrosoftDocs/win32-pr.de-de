---
description: Die GetCountOfType-Methode ruft rekursiv die Anzahl der Objekte eines angegebenen Typs ab, die in dieser Komposition enthalten sind, sowie alle zugehörigen virtuellen Spuren.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: IAMTimelineComp::GetCountOfType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b0504a7adb41a0d6a45714090a39aeefda9a3ef53b2d834540f600ec3ef871a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756410"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>IAMTimelineComp::GetCountOfType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetCountOfType` -Methode ruft rekursiv die Anzahl der Objekte eines angegebenen Typs ab, die in dieser Komposition enthalten sind, sowie alle zugehörigen virtuellen Spuren.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt rekursiv die Anzahl der Objekte des angegebenen Typs, die in dieser Komposition enthalten sind, und alle zugehörigen virtuellen Spuren.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Empfängt die in *pVal* zurückgegebene Anzahl sowie die Anzahl der gesuchten Kompositionen, einschließlich dieser.

</dd> <dt>

*MajorType* 
</dt> <dd>

Member des enumerierten [**TIMELINE \_ MAJOR \_ TYPE-Typs,**](timeline-major-type.md) der den Typ des zu zählenden Objekts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK zurück, \_ andernfalls E POINTER.

## <a name="remarks"></a>Hinweise

In der Regel ruft eine Anwendung diese Methode nicht auf. Sie wird von der Render-Engine aufgerufen.

Wenn Sie Kompositionen zählen, ist der in *pVal* zurückgegebene Wert 0 (null), und der in *pValWithComps* zurückgegebene Wert ist die Anzahl der Kompositionen. Der Wert von *\* pValWithComps* enthält die Komposition, für die Sie die -Methode aufrufen. Wenn Sie diese Methode beispielsweise für eine leere Komposition aufrufen, *\* entspricht pValWithComps* 1.

Gruppen können sich nicht in Kompositionen befinden, sodass Sie diese Methode nicht zum Zählen von Gruppen verwenden können. (Die zurückgegebene Anzahl ist immer null.) Um Gruppen zu zählen, rufen Sie die [**IAMTimeline::GetGroupCount-Methode**](iamtimeline-getgroupcount.md) auf.

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

[**IAMTimelineComp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





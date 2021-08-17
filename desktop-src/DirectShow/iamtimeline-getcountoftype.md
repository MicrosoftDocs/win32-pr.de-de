---
description: Die GetCountOfType-Methode ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Objekten enthalten sind.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: IAMTimeline::GetCountOfType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e9eb896f00752c5d9369cf494e7b1426347f82a7ebe2aac74f7822a936c2ffb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401061"
---
# <a name="iamtimelinegetcountoftype-method"></a>IAMTimeline::GetCountOfType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetCountOfType` -Methode ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Objekten enthalten sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppe* 
</dt> <dd>

Indexnummer der Gruppe, für die die Anzahl abgerufen werden soll.

</dd> <dt>

*pVal* 
</dt> <dd>

Empfängt rekursiv die Anzahl der Objekte des angegebenen Typs, die in der Gruppe enthalten sind, und alle zugehörigen virtuellen Spuren.

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

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültige Gruppennummer.<br/>      |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | **NULL-Zeigerargument.**<br/> |



 

## <a name="remarks"></a>Hinweise

Das Aufrufen dieser Methode entspricht dem Aufrufen von [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) für die angegebene Gruppe. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieser Methode.

In der Regel ruft eine Anwendung diese Methode nicht auf. Sie wird intern von der Render-Engine aufgerufen.

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

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





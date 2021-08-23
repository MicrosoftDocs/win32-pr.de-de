---
description: Die FixTimes-Methode rundet die angegebenen Start- und Stoppzeiten auf die nächsten Rahmengrenzen, wie in der Einstellung für die Bildfrequenz der übergeordneten Gruppe definiert.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: IAMTimelineObj::FixTimes-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6578b18e98c99b471097c98e9dd75de1cdce0c134635cad1fb17e32340eb1a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428420"
---
# <a name="iamtimelineobjfixtimes-method"></a>IAMTimelineObj::FixTimes-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode rundet die angegebenen Start- und Stoppzeiten auf die nächsten Rahmengrenzen, wie in der Einstellung für die Bildfrequenz der `FixTimes` übergeordneten Gruppe definiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in Einheiten von 100 Nanosekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Einheiten von 100 Nanosekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder E \_ NOTINTREE, wenn das Objekt nicht Teil einer Gruppe ist.

## <a name="remarks"></a>Hinweise

Während des Renderings rundet DES die Start- und Stoppzeiten des Objekts auf die nächste Framegrenze. Des überschreibt jedoch nicht die Zeiten des Objekts. Wenn Sie die Gruppenbildrate ändern, werden die gerundeten Zeiten immer anhand der ursprünglichen Zeiten berechnet. Weitere Informationen finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Verwenden Sie diese Methode, um genaue Start- und Stoppzeiten im gerenderten Projekt zu bestimmen. Beispielsweise sollten Sie die gerundeten Zeiten anstelle der ursprünglichen Start- und Endzeiten des Objekts suchen. Rufen [**Sie IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) auf, um die ursprünglichen Zeiten zu erhalten, und übergeben Sie diese Werte an `FixTimes` .

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





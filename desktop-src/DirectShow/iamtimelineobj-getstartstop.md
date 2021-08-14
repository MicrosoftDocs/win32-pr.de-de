---
description: Die GetStartStop-Methode ruft die Start- und Stoppzeiten des Objekts relativ zum übergeordneten Element des Objekts ab.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: IAMTimelineObj::GetStartStop-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400786"
---
# <a name="iamtimelineobjgetstartstop-method"></a>IAMTimelineObj::GetStartStop-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode ruft die Start- und Stoppzeiten des Objekts `GetStartStop` relativ zum übergeordneten Element des Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Empfängt die Startzeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*Pstop* 
</dt> <dd>

Empfängt die Stoppzeit in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Kompositionen, Gruppen und Spuren haben immer eine Startzeit von 0.

Während des Renderings rundet DES die Start- und Stoppzeiten eines Objekts auf die nächste Framegrenze. Des überschreibt jedoch nicht die Zeiten des Objekts. Wenn Sie die Gruppenbildrate ändern, werden die gerundeten Zeiten immer anhand der ursprünglichen Zeiten berechnet. Weitere Informationen finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Um die Start- und Stoppzeiten im gerenderten Projekt zu bestimmen, übergeben Sie die von zurückgegebenen Werte an die `GetStartStop` [**IAMTimelineObj::FixTimes-Methode.**](iamtimelineobj-fixtimes.md)

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





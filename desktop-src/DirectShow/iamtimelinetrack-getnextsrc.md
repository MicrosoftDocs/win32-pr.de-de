---
description: Die GetNextSrc-Methode durchsucht die Spur nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: IAMTimelineTrack::GetNextSrc-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd0257fa614a6581cc31f5416e6f1c2395fcb9444721d3668c9f2d2498e52088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904640"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>IAMTimelineTrack::GetNextSrc-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetNextSrc` -Methode durchsucht die Spur nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSrc* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Quellobjekts.

</dd> <dt>

*Pinout* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit für die Suche in Einheiten von 100 Nanosekunden enthält. Wenn die -Methode eine Quelle abruft, legt sie den Wert auf die Stoppzeit der Quelle fest. Wenn die Methode keine Quelle abruft, wird der Wert ungültig, und die Anwendung sollte ihn nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode eine Quelle abruft, andernfalls S \_ FALSE.

## <a name="remarks"></a>Hinweise

Wenn die von *pInOut* angegebene Zeit zwischen den Start- und Stoppzeiten einer Quelle liegt, ruft die Methode diese Quelle ab.

Wenn die Methode S \_ OK zurückgibt, verfügt **die IAMTimelineObj-Schnittstelle,** die sie zurückgibt, über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





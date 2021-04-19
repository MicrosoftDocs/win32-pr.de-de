---
description: Mit der fixtimes-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Iamtimelineobj:: fixtimes-Methode (qedit. h)'
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
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362172"
---
# <a name="iamtimelineobjfixtimes-method"></a>Iamtimelineobj:: fixtimes-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

`FixTimes`Mit der-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in 100-Nanosecond-Einheiten enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in 100-Nanosecond-Einheiten enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder E \_ notintree zurück, wenn das Objekt nicht Teil einer Gruppe ist.

## <a name="remarks"></a>Bemerkungen

Während des Renderings rundet der die Start-und Endzeit des Objekts auf die nächste Frame Grenze. Allerdings werden die Zeiten des Objekts von der nicht überschrieben. Wenn Sie die Gruppen Frame Rate ändern, werden die gerundeten Zeiten immer aus den ursprünglichen Zeiten berechnet. Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).

Verwenden Sie diese Methode, um genaue Start-und Endzeit im gerenderten Projekt zu bestimmen. Sie sollten z. b. die gerundeten Zeiten statt der ursprünglichen Start-und Endzeit des Objekts suchen. Rufen Sie [**iamtimelineobj:: getstarthalte**](iamtimelineobj-getstartstop.md) auf, um die ursprünglichen Zeiten abzurufen, und übergeben Sie diese Werte an `FixTimes` .

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





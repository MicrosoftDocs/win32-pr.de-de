---
description: Die getstartend-Methode ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Iamtimelineobj:: getstartstoppt-Methode (qedit. h)'
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
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360394"
---
# <a name="iamtimelineobjgetstartstop-method"></a>Iamtimelineobj:: getstartstoppt-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetStartStop` -Methode ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Empfängt die Startzeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*pstopps* 
</dt> <dd>

Empfängt die Endzeit in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Komposition, Gruppen und Spuren haben immer eine Startzeit von 0.

Während des Renderings rundet der die Start-und Endzeit eines Objekts auf die nächste Frame Grenze. Allerdings werden die Zeiten des Objekts von der nicht überschrieben. Wenn Sie die Gruppen Frame Rate ändern, werden die gerundeten Zeiten immer aus den ursprünglichen Zeiten berechnet. Weitere Informationen finden Sie unter [DirectShow-Bearbeitungs Dienste](time-in-directshow-editing-services.md).

Um die Start-und Endzeiten im gerenderten Projekt zu bestimmen, übergeben Sie die von zurückgegebenen Werte `GetStartStop` an die [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md) -Methode.

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

 

 





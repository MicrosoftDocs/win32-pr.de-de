---
description: 'Die ModifyStopTime2-Methode legt die Endzeit fest. Diese Methode entspricht iamtimelinesrc:: modifystoptime, aber nimmt einen reftime-Wert an.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Iamtimelinesrc:: ModifyStopTime2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370819"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>Iamtimelinesrc:: ModifyStopTime2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `ModifyStopTime2` Methode legt die Endzeit fest. Diese Methode entspricht [**iamtimelinesrc:: modifystoptime**](iamtimelinesrc-modifystoptime.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Beenden* 
</dt> <dd>

Neue Endzeit in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder E \_ invalidArg zurück, wenn die angegebene Zeit nicht gültig ist.

## <a name="remarks"></a>Bemerkungen

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





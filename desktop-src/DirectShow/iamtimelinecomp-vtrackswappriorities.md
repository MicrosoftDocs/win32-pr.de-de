---
description: Die vtracktauappriority-Methode schaltet die Prioritätsstufen von zwei nach Titeln um.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Iamtimelinecomp:: vtracktauapprioritäten-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354840"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>Iamtimelinecomp:: vtracktauapprioritäten-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `VTrackSwapPriorities` Methode schaltet die Prioritäts Ebenen von zwei-Spuren um.

Bei zwei Prioritätsstufen schaltet diese Methode die virtuellen Spuren in diese Prioritäten. Wenn die-Methode zurückgibt, befindet sich der Titel, der sich auf der ersten Prioritäts Ebene befand, jetzt auf der zweiten Prioritätsstufe (und umgekehrt).

## <a name="syntax"></a>Syntax


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Virtualtracka* 
</dt> <dd>

Die erste Prioritätsstufe, bei der virtuelle Spuren ausgetauscht werden sollen.

</dd> <dt>

*Virtualtrackb* 
</dt> <dd>

Die zweite Prioritätsstufe, bei der virtuelle Spuren ausgetauscht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

[**Iamtimelinecomp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





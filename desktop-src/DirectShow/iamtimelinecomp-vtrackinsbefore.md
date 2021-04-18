---
description: Die vtrackinsbefore-Methode fügt eine virtuelle Spur mit der angegebenen Priorität in die Komposition ein.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Iamtimelinecomp:: vtrackinsbefore-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354755"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>Iamtimelinecomp:: vtrackinsbefore-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `VTrackInsBefore` Methode fügt eine virtuelle Spur mit der angegebenen Priorität in die Komposition ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvirtualtrack* 
</dt> <dd>

Ein Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des virtuellen Titels.

</dd> <dt>

*Priority* 
</dt> <dd>

Die Priorität, mit der der virtuelle Track eingefügt werden soll, oder – 1, um den virtuellen Titel am Ende der Prioritäts Liste einzufügen. Die Prioritäts Liste bestimmt, welche Clips sichtbar sind. Weitere Informationen finden Sie unter Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiges Argument.<br/>              |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | Das Objekt ist kein virtueller Titel.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Jeder virtuelle Titel in der Komposition verfügt über eine eindeutige Prioritätsstufe. Die Prioritätsstufen liegen zwischen 0 und *n* -1, wobei *n* die Anzahl der virtuellen Spuren in der Komposition ist. Bei Video Gruppen verbirgt eine virtuelle Spur alle virtuellen Spuren mit einer niedrigeren Prioritätsstufe, außer an Orten, an denen der Titel leer ist oder einen Übergang enthält. Virtuelle Spuren können als Ebenen in der endgültigen Komposition betrachtet werden. Track 1 ist oberhalb von Track 0, Track 2 oberhalb von Track 1 und so weiter.

Wenn Sie-1 für den *Priority* -Parameter angeben, wird der virtuelle Track am Ende der Liste mit einem höheren Prioritätswert als die vorhandenen Spuren eingefügt. Wenn Sie einen Prioritätswert angeben, der bereits in der Komposition vorhanden ist, wird jede Spur mit der gleichen oder höheren Priorität um eine Prioritätsstufe nach oben verschoben.

**Beispiel**: Nachverfolgung A hat Priorität 0, und Track B hat Priorität 1. Wenn Track C mit Priorität 0 eingefügt wird, verfolgen Sie eine Verschiebung zu Priorität 1, und Nachverfolgen B wechselt zu Priorität 2.

Wenn die angegebene Priorität größer ist als die aktuelle Anzahl von Spuren in der Komposition, schlägt die Methode fehl.

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

 

 





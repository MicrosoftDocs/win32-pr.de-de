---
description: Die setgedämpf-Methode legt den gedämpften Zustand des Objekts fest. Ein mutobjekt wird nicht gerendert, aber es bleibt in der Zeitachse.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Iamtimelineobj:: setgedämpf-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361615"
---
# <a name="iamtimelineobjsetmuted-method"></a>Iamtimelineobj:: setgedämpf-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetMuted` -Methode legt den gedämpften Zustand des-Objekts fest. Ein mutobjekt wird nicht gerendert, aber es bleibt in der Zeitachse.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* 
</dt> <dd>

Flag, das den Zustand "stumm" angibt. **True** gibt an, dass das-Objekt und alle untergeordneten Elemente stumm geschaltet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Durch das Muting eines Objekts werden auch alle untergeordneten Elemente des-Objekts stumm. Wenn Sie z. b. eine Spur stumm schalten, werden die Übergänge, Quellen und Effekte in dieser Spur ebenfalls stumm geschaltet. Wenn das Objekt nicht mehr stumm geschaltet wird, werden die untergeordneten Elemente in ihren vorherigen Zustand zurückversetzt, der möglicherweise stumm oder unstumm ist.

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

 

 





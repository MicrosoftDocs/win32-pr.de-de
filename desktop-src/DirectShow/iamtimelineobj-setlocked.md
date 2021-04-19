---
description: Die setlocked-Methode legt den Bearbeitungs Zustand des-Objekts auf gesperrt oder entsperrt fest.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Iamtimelineobj:: setlocked-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359690"
---
# <a name="iamtimelineobjsetlocked-method"></a>Iamtimelineobj:: setlocked-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetLocked` -Methode legt den Bearbeitungs Zustand des-Objekts auf gesperrt oder entsperrt fest.

Ein gesperrter Zustand zeigt an, dass das Objekt nicht bearbeitet werden sollte. ein Entsperrter Zustand gibt an, dass das Objekt bearbeitet werden kann. Die Zeitachse erzwingt die Sperre nicht. Die Einstellung gesperrt ist nur für die praktische Verwendung der Anwendung vorhanden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* 
</dt> <dd>

Boolescher Wert, der den Bearbeitungs Zustand des-Objekts angibt. **True** gibt an, dass das Objekt gesperrt ist und nicht bearbeitet werden sollte. Wenn der Wert **false** ist, wird das Objekt entsperrt und kann bearbeitet werden.

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





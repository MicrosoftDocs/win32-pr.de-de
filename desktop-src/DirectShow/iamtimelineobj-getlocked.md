---
description: Die getlocked-Methode ruft den Bearbeitungsstatus des Objekts ab (gesperrt oder entsperrt).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Iamtimelineobj:: getlocked-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365579"
---
# <a name="iamtimelineobjgetlocked-method"></a>Iamtimelineobj:: getlocked-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetLocked` -Methode ruft den Bearbeitungs Zustand des-Objekts (gesperrt oder entsperrt) ab. Ein gesperrter Zustand zeigt an, dass das Objekt nicht bearbeitet werden sollte. ein Entsperrter Zustand gibt an, dass das Objekt bearbeitet werden kann. Die Zeitachse erzwingt die Sperre nicht. Die Einstellung gesperrt ist nur für die praktische Verwendung der Anwendung vorhanden.

## <a name="syntax"></a>Syntax


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt den Bearbeitungs Zustand des-Objekts. Wenn der Wert **true** ist, wird das Objekt gesperrt und sollte nicht bearbeitet werden. Wenn der Wert **false** ist, wird das Objekt entsperrt und kann bearbeitet werden.

</dd> </dl>

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

 

 





---
description: Die splicewithnext-Methode verbindet das Quell Objekt mit einem anderen Quell Objekt.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Iamtimelinesrc:: splicewithnext-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369962"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>Iamtimelinesrc:: splicewithnext-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SpliceWithNext` Methode verbindet das Quell Objekt mit einem anderen Quell Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNext* 
</dt> <dd>

Ein Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts, das mit der aktuellen Quelle verknüpft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                                      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiges Argument.<br/>                                             |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | Das durch den *pNext* -Parameter angegebene Objekt ist kein Quell Objekt.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument.<br/>                                    |



 

## <a name="remarks"></a>Bemerkungen

Wie momentan implementiert, verwirft diese Methode alle Auswirkungen auf *pNext*.

Damit diese Methode erfolgreich ausgeführt werden kann, muss *pNext* ein Übereinstimmungs Rahmen des aktuellen Quell Objekts sein, das wie folgt definiert wird:

-   Die gleiche Quelldatei muss gemeinsam genutzt werden.
-   Die Start Zeit des Mediums muss der Medien Endzeit der aktuellen Quelle entsprechen.
-   Die Wiedergabe Rate muss identisch sein. Die Wiedergabe Rate ist die Medien Dauer dividiert durch die Zeitachsen Dauer.

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

 

 





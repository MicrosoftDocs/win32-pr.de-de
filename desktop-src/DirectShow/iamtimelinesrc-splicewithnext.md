---
description: Die SpliceWithNext-Methode verbindet das Quellobjekt mit einem anderen Quellobjekt.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: IAMTimelineSrc::SpliceWithNext-Methode (Qedit.h)
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
ms.openlocfilehash: 1ffde9c7bb0416f2b296f7a7c347a058734430be33ef4ecde59e7e39cd6e845f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154831"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>IAMTimelineSrc::SpliceWithNext-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SpliceWithNext` -Methode verbindet das Quellobjekt mit einem anderen Quellobjekt.

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

Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Quellobjekts, das mit der aktuellen Quelle verknüpft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Rückgabewerte sind:



| Rückgabecode                                                                                   | Beschreibung                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiges Argument.<br/>                                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Das durch *den pNext-Parameter* angegebene Objekt ist kein Quellobjekt.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | **NULL-Zeigerargument.**<br/>                                    |



 

## <a name="remarks"></a>Hinweise

Wie derzeit implementiert, verwirft diese Methode alle Auswirkungen auf *pNext*.

Damit diese Methode erfolgreich ist, muss *pNext* ein Übereinstimmungsrahmen des aktuellen Quellobjekts sein, das wie folgt definiert ist:

-   Sie muss dieselbe Quelldatei gemeinsam nutzen.
-   Die Startzeit des Mediums muss der Medienstoppzeit der aktuellen Quelle entsprechen.
-   Die Wiedergaberate muss identisch sein. Die Wiedergaberate ist die Mediendauer geteilt durch die Dauer der Zeitachse.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





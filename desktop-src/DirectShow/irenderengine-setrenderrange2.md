---
description: Die SetRenderRange2-Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert werden soll. Diese Methode entspricht dem Wert von "tyenderengine::-Trend Modul Range", aber nimmt Werte vom Typ "Double" an.
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Unenderengine:: SetRenderRange2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358669"
---
# <a name="irenderenginesetrenderrange2-method"></a>Unenderengine:: SetRenderRange2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetRenderRange2` Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert wird. Diese Methode entspricht dem Wert von " [**tyenderengine::-Trend Modul Range**](irenderengine-setrenderrange.md)", aber nimmt Werte vom Typ " **Double**" an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* 
</dt> <dd>

Startzeit in Sekunden.

</dd> <dt>

*Beenden* 
</dt> <dd>

Endzeit in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl> | Fehler beim Initialisieren der Rendering-Engine.<br/> |



 

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

[**Schnittstelle ""**](irenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 





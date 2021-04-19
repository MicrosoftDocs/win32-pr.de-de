---
description: Die setrenderrange-Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert werden soll. Objekte, die sich außerhalb des angegebenen Bereichs befinden, werden nicht gerendert, und Ressourcen werden nicht zugeordnet.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: "\"Unenderengine:: *\"-Methode (\"qedit. h\")"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369176"
---
# <a name="irenderenginesetrenderrange-method"></a>"Unenderengine:: *"-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetRenderRange` Methode legt den Zeitbereich auf der Zeitachse fest, der gerendert wird. Objekte, die sich außerhalb des angegebenen Bereichs befinden, werden nicht gerendert, und Ressourcen werden nicht zugeordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* 
</dt> <dd>

Startzeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*Beenden* 
</dt> <dd>

Endzeit in 100-Nanosecond-Einheiten.

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

 

 





---
description: Die gettimelineobject-Methode ruft die Zeitachse ab, die von der Rendering-Engine zurzeit verwendet wird.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Unenderengine:: gettimelineobject-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366807"
---
# <a name="irenderenginegettimelineobject-method"></a>Unenderengine:: gettimelineobject-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetTimelineObject` Methode ruft die Zeitachse ab, die die Renderingengine zurzeit verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pptimeline* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimeline**](iamtimeline.md) -Schnittstelle der Zeitachse. Wenn keine Zeitachse vorhanden ist, erhält Sie den Wert **null** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>              | Ungültiger Zeiger.<br/>                    |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl> | Fehler beim Initialisieren der Rendering-Engine.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn bei der Rückgabe der Wert von *\* pptimeline* ungleich **null** ist, weist die **iamtimeline** -Schnittstelle eine ausstehende Verweis Anzahl auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

 

 





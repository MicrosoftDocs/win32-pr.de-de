---
description: Die GetFilterGraph-Methode ruft ggf. das Filterdiagramm ab, das von der Render-Engine erstellt wurde.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: IRenderEngine::GetFilterGraph-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8208d886cd23dab797a9f89d3c050c9f46eff60c8cdd78c27c89dae7396c557a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397581"
---
# <a name="irenderenginegetfiltergraph-method"></a>IRenderEngine::GetFilterGraph-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetFilterGraph` -Methode ruft ggf. das Filterdiagramm ab, das von der Render-Engine erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppFG* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) des Filterdiagramms. Er empfängt den Wert **NULL,** wenn kein Filterdiagramm vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ MUSS \_ RENDERER INIT \_**</dt> </dl> | Fehler beim Initialisieren der Render-Engine.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>              | Ungültiger Zeiger.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**IRenderEngine::ConnectFrontEnd-Methode,**](irenderengine-connectfrontend.md) um das Front-End des Filterdiagramms zu erstellen. Verwenden Sie für die Vorschau die [**IRenderEngine::RenderOutputPins,**](irenderengine-renderoutputpins.md) um das Diagramm zu vervollständigen. Verbinden Sie das Front-End für die Dateiausgabe mit einer Kombination aus Mux und Dateiwriter. Weitere Informationen finden Sie unter [Rendern eines Project](rendering-a-project.md).

Das resultierende Diagramm kann ausgeführt, angehalten, beendet und gesucht werden. Die Wiedergaberate kann jedoch nicht geändert werden.

Wenn der Wert von *\* ppFG* bei der Rückgabe ungleich **NULL** ist, weist die **IGraphBuilder-Schnittstelle** einen ausstehenden Verweiszähler auf. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: Die SetFilterGraph-Methode gibt ein Filterdiagramm für die zu verwendende Render-Engine an.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: IRenderEngine::SetFilterGraph-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4472d1152d45ee160885a4cdbc898a55ece24b6795a9880a5eeb958e05330287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767100"
---
# <a name="irenderenginesetfiltergraph-method"></a>IRenderEngine::SetFilterGraph-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetFilterGraph` -Methode gibt ein Filterdiagramm für die zu verwendende Render-Engine an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfg* 
</dt> <dd>

Zeiger auf die [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) des Filterdiagramms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Ungültiges Argument.<br/>                   |
| <dl> <dt>**E \_ MUSS \_ RENDERER INIT \_**</dt> </dl> | Fehler beim Initialisieren der Render-Engine.<br/> |



 

## <a name="remarks"></a>Hinweise

Die meisten Anwendungen müssen diese Methode nicht aufrufen. Es ist typischer, dass die Render-Engine das Diagramm für Sie erstellen lässt, indem sie die [**IRenderEngine::ConnectFrontEnd-Methode aufruft.**](irenderengine-connectfrontend.md)

Diese Methode schlägt fehl, wenn die Render-Engine bereits über ein Filterdiagramm verfügt.

Rufen Sie niemals einen Zeiger auf ein Filterdiagramm ab, das von einer Render-Engine erstellt wurde, und verwenden Sie ihn dann als Parameter für diese Methode in einer anderen Render-Engine. Dies führt zu unvorhersehbaren Ergebnissen.

Die **ConnectFrontEnd-Methode** entfernt alle vorhandenen Filterdiagramme, behält jedoch die gleiche Filter Graph Manager-Instanz bei.

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

 

 





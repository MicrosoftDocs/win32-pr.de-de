---
description: Die setfiltergraph-Methode gibt ein Filter Diagramm für die zu verwendende Rendering-Engine an.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Unenderengine:: setfiltergraph-Methode (qedit. h)'
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
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371564"
---
# <a name="irenderenginesetfiltergraph-method"></a>Unenderengine:: setfiltergraph-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetFilterGraph` Methode gibt ein Filter Diagramm für die zu verwendende Rendering-Engine an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PFG* 
</dt> <dd>

Ein Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Diagramms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>           | Ungültiges Argument.<br/>                   |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl> | Fehler beim Initialisieren der Rendering-Engine.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die meisten Anwendungen müssen diese Methode nicht aufzurufen. Es ist eher typisch, dass die Renderingengine das Diagramm für Sie erstellt, indem Sie die Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " aufrufen.

Diese Methode schlägt fehl, wenn die Renderingengine bereits über ein Filter Diagramm verfügt.

Rufen Sie niemals einen Zeiger auf ein Filter Diagramm ab, das von einem Rendermodul erstellt wurde, und verwenden Sie es dann als Parameter für diese Methode in einer anderen Renderingengine. Dies führt zu unvorhersehbaren Ergebnissen.

Die **connectfrontend** -Methode führt ein beliebiges vorhandenes Filter Diagramm aus, behält aber dieselbe Filter-Graph-Manager-Instanz bei.

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

 

 





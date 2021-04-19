---
description: Die getfiltergraph-Methode ruft das Filter Diagramm ab, das von der Rendering-Engine erstellt wurde (sofern vorhanden).
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Unenderengine:: getfiltergraph-Methode (qedit. h)'
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
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356310"
---
# <a name="irenderenginegetfiltergraph-method"></a>Unenderengine:: getfiltergraph-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetFilterGraph` Methode ruft das Filter Diagramm ab, das von der Rendering-Engine erstellt wurde (sofern vorhanden).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppfg* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Diagramms. Er empfängt den Wert **null** , wenn kein Filter Diagramm vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl> | Fehler beim Initialisieren der Rendering-Engine.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>              | Ungültiger Zeiger.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) ", um das Front-End des Filter Diagramms zu erstellen. Verwenden Sie für die Vorschauversion den " [**unenderengine:: renderoutputpins**](irenderengine-renderoutputpins.md) ", um das Diagramm abzuschließen. Für die Dateiausgabe verbinden Sie das Front-End mit einer Kombination aus MUX/dateiwriter. Weitere Informationen finden Sie unter [Rendern eines Projekts](rendering-a-project.md).

Das resultierende Diagramm kann ausgeführt, angehalten, beendet und Seeding ausgeführt werden. die Wiedergabe Rate kann jedoch nicht geändert werden.

Wenn der Wert von *\* ppfg* bei Rückgabe ungleich **null** ist, weist die **igraphbuilder** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

 

 





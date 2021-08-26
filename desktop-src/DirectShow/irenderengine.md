---
description: 'Die IRenderEngine-Schnittstelle rendert ein Des-Projekt (DirectShow Editing Services), indem ein Filterdiagramm aus einer Zeitachse erstellt wird. DES stellt zwei Komponenten bereit, die diese Schnittstelle implementieren: Die einfache Render-Engine erstellt eine unkomprimierte Ausgabe.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: IRenderEngine-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a13d51eb41a917dc4790c75a8a1f8a881dbcb8489364722ff8805bdf26fc77f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051310"
---
# <a name="irenderengine-interface"></a>IRenderEngine-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IRenderEngine` Schnittstelle rendert ein [DES-Projekt (DirectShow Editing Services),](directshow-editing-services.md) indem ein Filterdiagramm aus einer Zeitachse erstellt wird.

DES stellt zwei Komponenten bereit, die diese Schnittstelle implementieren:

-   Die *einfache Render-Engine* erstellt eine unkomprimierte Ausgabe. Sie können die Ausgabe für die Vorschau verwenden oder sie über Komprimierungsfilter routen und in eine Datei schreiben.
-   Die *intelligente Render-Engine* erstellt mithilfe der *intelligenten Rekomprimierung komprimierte Ausgaben.* Bei der intelligenten Rekomprimierung wird eine Quelldatei nur dann erneut komprimiert, wenn sich ihr Format vom Ausgabeformat unterscheidet. Eine Quelle mit einem übereinstimmenden Format wird direkt in die Ausgabedatei geschrieben. Je nach Szenario kann die intelligente Rekomprimierung die Renderingzeit stark verbessern.

Die intelligente Render-Engine unterstützt auch die [**ISmartRenderEngine-Schnittstelle.**](ismartrenderengine.md)

Obwohl eine Anwendung ein Filterdiagramm erstellen und an eine Render-Engine übergeben kann, ist das typische Szenario, dass die Render-Engine das Filterdiagramm erstellt. Das Erstellen des Graphen ist ein zweistufiger Prozess. Erstellen Sie zunächst das Front-End, indem Sie die [**IRenderEngine::ConnectFrontEnd-Methode**](irenderengine-connectfrontend.md) aufrufen. Verbinden Sie dann die Ausgabepins am Front-End mit den gewünschten Renderingfiltern:

-   Video- und Audiorenderer für die Vorschau oder
-   Erz-, Multiplexer- und Dateischreiber, um die endgültige Ausgabe zu generieren.

## <a name="members"></a>Member

Die **IRenderEngine-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IRenderEngine-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**begehen**](irenderengine-commit.md)                                             | Nicht implementiert.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Erstellt das Front-End des Filterdiagramms aus der aktuellen Zeitachse.<br/>        |
| [**Decommit**](irenderengine-decommit.md)                                         | Nicht implementiert.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | Wird nicht unterstützt.<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | Nicht implementiert.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Ruft das Filterdiagramm ab, das die Render-Engine erstellt hat, sofern dies der Fall ist.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Ruft den Ausgabepin für die angegebene Gruppe ab.<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | Ruft die Zeitachse ab, die die Render-Engine derzeit verwendet.<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | Ruft die Anbieterzeichenfolge ab.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Erstellt den Vorschaubereich des Filterdiagramms.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Verwirft das Filterdiagramm der Render-Engine und alle zugeordneten Objekte.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Gibt ein Filterdiagramm an, das von der Render-Engine verwendet werden soll.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | Wird nicht unterstützt.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | Wird nicht unterstützt.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Legt den Zeitbereich fest, der gerendert werden soll.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Legt den Zeitbereich, der gerendert werden soll, als double **fest.**<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | Wird nicht unterstützt.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Gibt an, wie die Render-Engine Dateinamen überprüft.<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | Legt die Zeitachse für die zu verwendende Render-Engine fest.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | Wird nicht unterstützt.<br/>                                                             |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Rendern eines Project](rendering-a-project.md)
</dt> </dl>

 

 

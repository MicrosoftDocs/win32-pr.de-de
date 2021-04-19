---
description: 'Die Schnittstelle "" wird durch das Erstellen eines Filter Diagramms aus einer Zeitachse ein Projekt vom Typ "DirectShow-Bearbeitungs Dienste" gerendert. Des bietet zwei Komponenten, die diese Schnittstelle implementieren: die einfache Renderingengine erstellt eine unkomprimierte Ausgabe.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Unenderengine-Schnittstelle (qedit. h)
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
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370811"
---
# <a name="irenderengine-interface"></a>Schnittstelle ""

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IRenderEngine` Schnittstelle rendert ein [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) -Projekt durch Erstellen eines Filter Diagramms aus einer Zeitachse.

DES bietet zwei Komponenten, die diese Schnittstelle implementieren:

-   Die *einfache Renderingengine* erstellt eine nicht komprimierte Ausgabe. Sie können die Ausgabe für die Vorschau verwenden oder Sie durch Komprimierungs Filter weiterleiten und in eine Datei schreiben.
-   Die *Smart-Rendering-Engine* erstellt mithilfe der *intelligenten Neukomprimierung* eine komprimierte Ausgabe. Bei intelligenter Neukomprimierung wird eine Quelldatei nur dann erneut komprimiert, wenn sich ihr Format vom Ausgabeformat unterscheidet. Eine Quelle mit einem übereinstimmenden Format wird direkt in die Ausgabedatei geschrieben. Je nach Szenario kann die Renderingzeit durch intelligente Neukomprimierung erheblich verbessert werden.

Die Smart-Rendering-Engine unterstützt auch die [**ismartrenderengine**](ismartrenderengine.md) -Schnittstelle.

Obwohl eine Anwendung ein Filter Diagramm erstellen und an eine Renderingengine übergeben kann, besteht das typische Szenario darin, dass die Renderingengine das Filter Diagramm erstellt. Der Aufbau des Diagramms ist ein zweistufiger Prozess. Erstellen Sie zuerst das Front-End, indem Sie die Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " aufrufen. Verbinden Sie anschließend die Ausgabe Pins auf dem Front-End mit den gewünschten renderingfiltern:

-   Video-und audiorenderer für die Vorschauversion oder
-   Kompressoren, Multiplexer und Datei Schreiber, um die endgültige Ausgabe zu generieren.

## <a name="members"></a>Member

Die Schnittstelle " **irienderengine** " erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. " **Irienderengine** " verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die " **irienderengine** "-Schnittstelle verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Einzusetzen**](irenderengine-commit.md)                                             | Nicht implementiert.<br/>                                                           |
| [**Connectfrontend**](irenderengine-connectfrontend.md)                           | Erstellt das Front-End des Filter Diagramms aus der aktuellen Zeitachse.<br/>        |
| [**Decommit**](irenderengine-decommit.md)                                         | Nicht implementiert.<br/>                                                           |
| [**Dosmartrecompression**](irenderengine-dosmartrecompression.md)                 | Wird nicht unterstützt.<br/>                                                             |
| [**Getcaps**](irenderengine-getcaps.md)                                           | Nicht implementiert.<br/>                                                           |
| [**Getfiltergraph**](irenderengine-getfiltergraph.md)                             | Ruft das Filter Diagramm ab, das von der Rendering-Engine erstellt wurde (sofern vorhanden).<br/> |
| [**Getgroupoutputpin**](irenderengine-getgroupoutputpin.md)                       | Ruft die Ausgabepin für die angegebene Gruppe ab.<br/>                          |
| [**Gettimelineobject**](irenderengine-gettimelineobject.md)                       | Ruft die Zeitachse ab, die von der Rendering-Engine zurzeit verwendet wird.<br/>          |
| [**Getvendorstring**](irenderengine-getvendorstring.md)                           | Ruft die Hersteller Zeichenfolge ab.<br/>                                               |
| [**Renderoutputpins**](irenderengine-renderoutputpins.md)                         | Erstellt den Preview-Teil des Filter Diagramms.<br/>                        |
| [**Scrapit**](irenderengine-scrapit.md)                                           | Verwirft das Filter Diagramm der Rendering-Engine und alle zugeordneten Objekte.<br/>      |
| [**Setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)         | Legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.<br/>                   |
| [**Setfiltergraph**](irenderengine-setfiltergraph.md)                             | Gibt ein Filter Diagramm für die zu verwendende Rendering-Engine an.<br/>                     |
| [**Setinterestrange**](irenderengine-setinterestrange.md)                         | Wird nicht unterstützt.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | Wird nicht unterstützt.<br/>                                                             |
| [**"Strenderrange"**](irenderengine-setrenderrange.md)                             | Legt den Zeitbereich fest, der gerendert werden soll.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Legt den Zeitbereich, der gerendert werden soll, als **Double** fest.<br/>                    |
| [**Setsourceconnectcallback**](irenderengine-setsourceconnectcallback.md)         | Wird nicht unterstützt.<br/>                                                             |
| [**Setsourcenamevalidation**](irenderengine-setsourcenamevalidation.md)           | Gibt an, wie die Renderingengine Dateinamen überprüft.<br/>                      |
| [**Settimelineobject**](irenderengine-settimelineobject.md)                       | Legt die Zeitachse für die zu verwendende Rendering-Engine fest.<br/>                            |
| [**"US-smartrecompressiongraph"**](irenderengine-useinsmartrecompressiongraph.md) | Wird nicht unterstützt.<br/>                                                             |



 

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

[Rendern eines Projekts](rendering-a-project.md)
</dt> </dl>

 

 

---
description: In diesem Abschnitt wird beschrieben, wie die Pfad bezogenen Schnittstellen der XPS-Dokument-API in einem XPS-OM verwendet werden.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Arbeiten mit XPS-OM-Pfad Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca66b65c6f20dc3b585de706e223df1f76d518a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529354"
---
# <a name="working-with-xps-om-path-interfaces"></a>Arbeiten mit XPS-OM-Pfad Schnittstellen

In diesem Abschnitt wird beschrieben, wie die Pfad bezogenen Schnittstellen der XPS-Dokument-API in einem XPS-OM verwendet werden.



| Schnittstellen Name                                                            | Konzeptionelle untergeordnete Elemente                                                                                                                                                                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Beschreibt ein grafisches Pfad Element.<br/>                                                                                                                                                    |
| [**Ixpsombrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**Ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**Ixpsomtilebrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**Ixpsomvisualbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**Ixpsomimagebrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**Ixpsomgradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**Ixpsomlineargradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**Ixpsomradialgradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Ein Pinsel wird verwendet, um einen Bereich oder eine Linie auszufüllen.<br/>                                                                                                                                             |
| [**Ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Bietet voll Tonfarbe oder Striche. <br/>                                                                                                                                                |
| [**Ixpsomvisualbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Stellt ein visuelles Objekt bereit, z. b. einen Pfad, ein Symbol oder eine Canvas oder eine partielle Visualisierung, die als ein-oder-Strich verwendet werden soll. <br/>                                                                  |
| [**Ixpsomimagebrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Stellt ein Bild (oder partielles Bild) bereit, das als ein-oder-Strich verwendet werden soll. <br/>                                                                                                           |
| [**Ixpsomlineargradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Stellt einen linearen Farbverlauf bereit, der als Füll-oder Strich verwendet werden soll. <br/>                                                                                                                            |
| [**Ixpsomradialgradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Stellt einen radialen Farbverlauf bereit, der als Füll-oder Strich verwendet werden soll. <br/>                                                                                                                            |
| [**Ixpsomgradientstoppt**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Definiert einen einzelnen Farbwert innerhalb eines linearen oder radialen Farbverlaufs. <br/>                                                                                                     |
| [**Ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**Ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Stellt eine Definition eines Vektor Bereichs bereit, der als Clippingbereich oder Pfad Definition verwendet werden soll. Besteht aus mindestens einer [**ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) -Schnittstelle. <br/> |
| [**Ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Teil einer Regions Definition, auf die von einer [**ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) -Schnittstelle verwiesen wird und die aus einem oder mehreren Segmenten besteht. <br/>                                    |
| [**Ixpsommatrixtransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Gibt die affinine Matrix Transformation an, die während des Renderings auf das-Objekt angewendet werden soll. <br/>                                                                                              |



 

## <a name="contents"></a>Inhalte

-   [XPS-OM-Pinsel](xps-object-model-brushes.md)
-   [XPS-OM-Farbverläufe](xps-object-model-gradients.md)
-   [XPS OM-Geometry-Objekte](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ixpsompath-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Ixpsomdashcollection-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**Ixpsommatrixtransform-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 





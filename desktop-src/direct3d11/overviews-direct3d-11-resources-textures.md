---
title: Texturen
description: In diesem Abschnitt werden die in Direct3D 11 verwendeten Texturen und Links zur aufgabenbasierten Dokumentation für gängige Szenarios beschrieben.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207075"
---
# <a name="textures"></a>Texturen

In einer Textur werden Texel-Informationen gespeichert. In diesem Abschnitt werden die in Direct3D 11 verwendeten Texturen und Links zur aufgabenbasierten Dokumentation für gängige Szenarios beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einführung in Texturen in Direct3D 11](overviews-direct3d-11-resources-textures-intro.md)<br/> | Eine Textur Ressource ist eine strukturierte Sammlung von Daten, die zum Speichern von texeln entwickelt wurden. Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder geschrieben werden kann. Im Gegensatz zu puffern können Texturen durch Textur-samplz gefiltert werden, wenn Sie von Shader-Einheiten gelesen werden. Der Typ der Textur wirkt sich darauf aus, wie die Textur gefiltert wird. Jede texumeration enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind, die durch die Enumeration des DXGI-Formats definiert werden \_ .<br/> |
| [Textur Block Komprimierung in Direct3D 11](texture-block-compression-in-direct3d-11.md)<br/>      | Block Komprimierungs Unterstützung (BC) für Texturen wurde in Direct3D 11 erweitert, um die BC6H-und bzw bc7-Algorithmen einzubeziehen. BC6H unterstützt Datenquellen Daten mit hoher dynamischer Bereichs Farbe, und bzw bc7 bietet eine bessere Qualitäts Komprimierung mit weniger Artefakten für Standard-RGB-Quelldaten.<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgehensweise: Erstellen einer Textur](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[Gewusst wie: Programm gesteuertes Initialisieren einer Textur](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[Gewusst wie: Initialisieren einer Textur aus einer Datei](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 






---
title: Texturen
description: In diesem Abschnitt werden Texturen beschrieben, die in Direct3D 11 verwendet werden, und Links zur aufgabenbasierten Dokumentation für häufige Szenarien.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e02fbc59922710aaf764dafd363429a68c734d365335f5bdb4355bec8570971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027840"
---
# <a name="textures"></a>Texturen

Eine Textur speichert Texelinformationen. In diesem Abschnitt werden Texturen beschrieben, die in Direct3D 11 verwendet werden, und Links zur aufgabenbasierten Dokumentation für häufige Szenarien.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einführung in Texturen in Direct3D 11](overviews-direct3d-11-resources-textures-intro.md)<br/> | Eine Texturressource ist eine strukturierte Sammlung von Daten zum Speichern von Texel. Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder in diese geschrieben werden kann. Im Gegensatz zu Puffern können Texturen von Textur-Samplern gefiltert werden, während sie von Shadereinheiten gelesen werden. Der Texturtyp wirkt sich darauf aus, wie die Textur gefiltert wird. Jedes Texel enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind, die durch die DXGI \_ FORMAT-Enumeration definiert werden.<br/> |
| [Texturblockkomprimierung in Direct3D 11](texture-block-compression-in-direct3d-11.md)<br/>      | Die Unterstützung der Blockkomprimierung für Texturen wurde in Direct3D 11 um die BC6H- und BC7-Algorithmen erweitert. BC6H unterstützt Farbquelldaten mit hohem dynamischen Bereich, und BC7 bietet eine bessere als die durchschnittliche Qualitätskomprimierung mit weniger Artefakten für RGB-Standardquelldaten.<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgehensweise: Erstellen einer Textur](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[Vorgehensweise: Programmgesteuertes Initialisieren einer Textur](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[Vorgehensweise: Initialisieren einer Textur aus einer Datei](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 






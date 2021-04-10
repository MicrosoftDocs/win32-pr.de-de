---
description: Diese Tabelle enthält eine Liste der minimalen Ressourcen, die von Direct3D 10 unterstützt werden.
ms.assetid: 79c13aed-87bd-4875-9810-c3e078f58753
title: Ressourcen Limits (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ea3e3a181605e548c4e9f0a8b69691564163799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041535"
---
# <a name="resource-limits-direct3d-10"></a>Ressourcen Limits (Direct3D 10)

Diese Tabelle enthält eine Liste der minimalen Ressourcen, die von Direct3D 10 unterstützt werden.



| Resource                                                                                               | Begrenzung                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Anzahl von Elementen in einem konstanten Puffer                                                                | 4096                                                 |
| Anzahl von texeln (unabhängig von der Struktur Größe) in einem Puffer                                              | 227 texeln                                           |
| Texture1D U-Dimension                                                                                  | 8192                                                 |
| Texture1DArray-Dimension                                                                               | 512 Array Slices                                     |
| Texture2D U/V-Dimension                                                                                | 8192                                                 |
| Texture2DArray-Dimension                                                                               | 512 Array Slices                                     |
| Texture3D U/V/W-Dimension                                                                              | 2048                                                 |
| Texturecube-Dimension                                                                                  | 8192                                                 |
| Ressourcen Größe (in MB)                                                                                  | 128 MB ¹                                              |
| Anisotrope Filterung MaxAnisotropy                                                                    | 16                                                   |
| Durch Filtern von Hardware adressierbare Ressourcen Dimension                                                   | 8192 pro Dimension                                   |
| Ressourcen Größe (in MB) adressierbar durch IA (Eingabe-oder Scheitelpunkt Daten) oder vs/GS/PS (Point Sample)              | 128 MB ¹                                              |
| Gesamtanzahl der Ressourcen Sichten pro Kontext (jedes Array zählt als 1) (alle Ansichts Typen haben Shared Limit) | 220                                                  |
| Größe der Puffer Struktur (Multielement)                                                                  | 2\.048 Bytes                                           |
| Streamausgabegröße                                                                                     | Identisch mit der Anzahl der texeln in einem Puffer (siehe oben) |
| Zeichnen oder drawinstanzierte Scheitelpunkt Anzahl (einschließlich Instanziierung)                                              | 232                                                  |
| Drawinabxed- \[ Instanziierung \] () Vertex-Anzahl (inkl. Instanziierung)                                             | 232                                                  |
| GS-Aufruf Ausgabedaten (Komponenten \* Vertices)                                                     | 1024                                                 |
| Gesamtanzahl von samplerobjekten pro Kontext                                                            | 4096                                                 |
| Gesamtanzahl der Viewport/Scissor-Objekte pro Pipeline                                                  | 16                                                   |
| Gesamtanzahl der Ausschneide-/Ausschneide Abstände pro Scheitelpunkt                                                         | 8                                                    |
| Gesamtanzahl von Blend-Objekten pro Kontext                                                              | 4096                                                 |
| Gesamtzahl der tiefen-/Stencil-Objekte pro Kontext                                                      | 4096                                                 |
| Gesamtanzahl der Raster-Zustands Objekte pro Kontext                                                   | 4096                                                 |
| Maximale Anzahl von Stichproben pro Pixel während der multisamplinggrad                                                    | 32                                                   |
| Shader-Ressourcen-Vertex-Element Anzahl (4 32-Bit-Komponenten)                                          | 16                                                   |
| Common-Shader Core (4 32-Bit-Komponenten) Temp-Register count (r \# + indizierbar x \# \[ n \] )             | 4096                                                 |
| Common-Shader-Kern Konstante: Puffer Slots                                                               | 14                                                   |
| Allgemeine Shader-Kern Eingabe-Ressourcen Slots                                                                | 128                                                  |
| Haupt-Sampler-Slots von Common-Shader                                                                       | 16                                                   |
| Haupt-Shader-Kern Unterroutine-Schachtelungs Limit                                                            | 32                                                   |
| Schachtelungs Limit für die Kern-Shader-Kern Fluss Steuerung                                                          | 64                                                   |
| Vertex-Shader-Eingabe-Register-Anzahl (4 32-Bit-Komponenten)                                            | 16                                                   |
| Vertex-Shader-Ausgabe: Register Anzahl (4 32-Bit-Komponenten)                                           | 16                                                   |
| Geometry-Shader-Eingabe-Register-Anzahl (4 32-Bit-Komponenten)                                          | 16                                                   |
| Geometry-Shader-Ausgabe: Registrierungs Anzahl (4 32-Bit-Komponenten)                                         | 32                                                   |
| Pixel-Shader-Eingabe-Register-Anzahl (4 32-Bit-Komponenten)                                             | 32                                                   |
| Pixel-Shader-Ausgabe: Register Anzahl (4 32-Bit-Komponenten)                                            | 8                                                    |
| Anzahl von Pixel-Shader-Ausgabe tiefen Register (32-Bit \* 1-Komponente)                                          | 1                                                    |
| Eingabe Ressourcen Slots für Eingabe Assembler Index                                                             | 1                                                    |
| Eingabe-Assembler-vertexeingabe-Ressourcen Slots                                                            | 16                                                   |



 

¹ Apps können Ressourcen erstellen, die größer als die maximale Ressourcen Größe auf einigen Grafikhardware sind. Es wird jedoch empfohlen, dass apps Ressourcen kleiner als die maximale Ressourcen Größe behalten, um die maximale Menge an Kompatibilität über Grafik Anbieter hinweg zu erhalten. Die Laufzeit gewährleistet nur, dass Belegungen innerhalb der maximalen Ressourcen Größe von allen Direct3D 10-Hardware unterstützt werden. Wenn eine APP versucht, Arbeitsspeicher für eine Ressource innerhalb der maximalen Ressourcen Größe zuzuweisen, schlägt die Laufzeit den Versuch nur fehl, wenn das Betriebssystem nicht über genügend Ressourcen verfügt. Wenn eine APP versucht, Arbeitsspeicher für eine Ressource über der maximalen Ressourcen Größe zuzuweisen, kann der Versuch der Laufzeit fehlschlagen, da entweder das Betriebssystem überschritten wird oder die Hardware keine Zuordnungen über der maximalen Ressourcen Größe unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




---
description: X Dateiformat-, Lade-und Speicheroptionen.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342930"
---
# <a name="d3dxf"></a>D3DXF

X Dateiformat-, Lade-und Speicheroptionen.

## <a name="file-formats"></a>Dateiformate

In der folgenden Tabelle sind die Datei Datentypen angegeben:



| \#definiert das Datei Format.     | Wert | BESCHREIBUNG                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ File Format- \_ Binärdatei     | 0     | Binärdatei im Legacy Format. Siehe [Referenz zu X-Dateien (Legacy)](dx9-graphics-reference-x-file.md). |
| D3DXF \_ File Format- \_ Text       | 1     | Textdatei.                                                                                     |
| D3DXF \_ File Format \_ komprimiert | 2     | Komprimierte Datei. Mit diesem Flag müssen Sie auch das Binärformat oder das Textformat angeben.   |



 

## <a name="file-load-options"></a>Optionen zum Laden von Dateien

In der folgenden Tabelle sind die Optionen zum Laden von Dateien mit x-Dateien angegeben:



| \#definieren                      | Wert | BESCHREIBUNG                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ fileload \_ FromFile     | 0     | Laden von Daten aus einer Datei.     |
| D3DXF \_ fileload \_ fromwfile    | 1     | Laden von Daten aus einer Datei.     |
| D3DXF \_ fileload \_ FromResource | 2     | Laden von Daten aus einer Ressource. |
| D3DXF \_ fileload \_ frommemory   | 3     | Laden von Daten aus dem Arbeitsspeicher.     |



 

## <a name="file-save-options"></a>Optionen zum Speichern von Dateien

In der folgenden Tabelle sind die Optionen zum Speichern und Laden von Dateien mit x-Dateien angegeben:



| \#definieren                 | Wert | BESCHREIBUNG                    |
|--------------------------|-------|--------------------------------|
| Datei "D3DXF \_ filesave" \_  | 0     | In einer Datei speichern.                |
| D3DXF \_ filesave \_ towfile | 1     | In einer breit Zeichen Datei speichern. |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3dx9xof. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX X-Datei Konstanten](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 




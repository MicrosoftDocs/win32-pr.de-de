---
description: Optionen für X-Dateiformat, Laden und Speichern.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d286ad4cf64133683de026893beb9fa081899e6b170e4b3adb478798eb4b3edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096075"
---
# <a name="d3dxf"></a>D3DXF

Optionen für X-Dateiformat, Laden und Speichern.

## <a name="file-formats"></a>Dateiformate

Die folgende Tabelle gibt den Typ der Dateidaten an:



| \#defines für Das Dateiformat     | Wert | Beschreibung                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ FILEFORMAT \_ BINARY     | 0     | Binärdatei im Legacyformat. Siehe [X-Dateireferenz (Legacy)](dx9-graphics-reference-x-file.md). |
| D3DXF \_ FILEFORMAT \_ TEXT       | 1     | Textdatei.                                                                                     |
| D3DXF \_ FILEFORMAT \_ COMPRESSED | 2     | Komprimierte Datei. Mit diesem Flag müssen Sie auch das Binärformat oder das Textformat angeben.   |



 

## <a name="file-load-options"></a>Dateiladeoptionen

In der folgenden Tabelle sind Dateiladeoptionen mit X-Dateien angegeben:



| \#Definieren                      | Wert | Beschreibung                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | Laden von Daten aus einer Datei.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Laden von Daten aus einer Datei.     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Laden von Daten aus einer Ressource. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Laden von Daten aus dem Arbeitsspeicher.     |



 

## <a name="file-save-options"></a>Dateispeicheroptionen

In der folgenden Tabelle werden Optionen zum Speichern und Laden von Dateien mit X-Dateien angegeben:



| \#Definieren                 | Wert | Beschreibung                    |
|--------------------------|-------|--------------------------------|
| D3DXF \_ FILESAVE \_ TOFILE  | 0     | Speichern sie in einer Datei.                |
| D3DXF \_ FILESAVE \_ TOWFILE | 1     | Speichern Sie in einer Breitzeichendatei. |



 

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3dx9xof.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX X-Dateikonstanten](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 




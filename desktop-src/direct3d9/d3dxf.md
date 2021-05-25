---
description: X-Dateiformat, Lade- und Speicheroptionen.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343645"
---
# <a name="d3dxf"></a>D3DXF

X-Dateiformat, Lade- und Speicheroptionen.

## <a name="file-formats"></a>Dateiformate

In der folgenden Tabelle wird der Typ der Dateidaten angegeben:



| \#definiert für Das Dateiformat.     | Wert | BESCHREIBUNG                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ FILEFORMAT \_ BINARY     | 0     | Binärdatei im Legacyformat. Weitere Informationen [finden Sie unter X-Dateireferenz (Legacy).](dx9-graphics-reference-x-file.md) |
| D3DXF \_ FILEFORMAT \_ TEXT       | 1     | Textdatei.                                                                                     |
| D3DXF \_ FILEFORMAT \_ COMPRESSED | 2     | Komprimierte Datei. Mit diesem Flag müssen Sie auch das Binärformat oder das Textformat angeben.   |



 

## <a name="file-load-options"></a>Optionen zum Laden von Dateien

In der folgenden Tabelle werden Optionen zum Laden von Dateien mit X-Dateien angegeben:



| \#Definieren                      | Wert | BESCHREIBUNG                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | Laden von Daten aus einer Datei.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Laden von Daten aus einer Datei.     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Laden von Daten aus einer Ressource. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Laden von Daten aus dem Arbeitsspeicher.     |



 

## <a name="file-save-options"></a>Dateispeicheroptionen

In der folgenden Tabelle werden Optionen zum Speichern und Laden von Dateien mit X-Dateien angegeben:



| \#Definieren                 | Wert | BESCHREIBUNG                    |
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

 

 




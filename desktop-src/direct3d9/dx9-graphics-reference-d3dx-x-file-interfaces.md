---
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen, die zum Lesen und Schreiben aus X-Dateien verwendet werden.
ms.assetid: 54d8a02b-5376-49ac-a0d5-fc3cd8ab82e6
title: D3DX X-Dateischnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db018f9bd7beca0ca81b441fb463e46026e8a011b22e8de5ccd6c0f3a596794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564360"
---
# <a name="d3dx-x-file-interfaces"></a>D3DX X-Dateischnittstellen

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen, die zum Lesen und Schreiben aus X-Dateien verwendet werden.

-   [**ID3DXFile**](id3dxfile.md)
-   [**ID3DXFileData**](id3dxfiledata.md)
-   [**ID3DXFileEnumObject**](id3dxfileenumobject.md)
-   [**ID3DXFileSaveData**](id3dxfilesavedata.md)
-   [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)

Die folgenden Tabellen veranschaulichen die Beziehung zwischen den X-Dateischnittstellen.



| Schnittstelle             | Wird von abgeleitet.           | Wird von abgeleitet. |
|-----------------------|------------------------|--------------|
|                       | IDirectXFile           | IUnknown     |
| IDirectXFileBinary    | IDirectXFileObject     | IUnknown     |
| IDirectXFileData      | IDirectXFileObject     | IUnknown     |
| IDirectXFileReference | IDirectXFileObject     | IUnknown     |
|                       | IDirectXFileSaveObject | IUnknown     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateiverweis](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 




---
description: Verwenden Sie das folgende Verfahren in Legacyanwendungen, um eine X-Datei zu laden.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Laden einer X-Datei (Legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8ac27c43ba33f6bd0408403d6390d4855f2644182d82f1ad8e84e5939f98ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846520"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Laden einer X-Datei (Legacy) (Direct3D 9)

Verwenden Sie das folgende Verfahren in Legacyanwendungen, um eine X-Datei zu laden.

1.  Verwenden Sie die [**DirectXFileCreate-Funktion,**](directxfilecreate.md) um ein [**IDirectXFile-Objekt zu**](idirectxfile.md) erstellen.
2.  Wenn Vorlagen in der DirectX-Datei vorhanden sind, die Sie laden möchten, verwenden Sie die [**IDirectXFile::RegisterTemplates-Methode,**](idirectxfile--registertemplates.md) um diese Vorlagen zu registrieren.
3.  Verwenden Sie [**die IDirectXFile::CreateEnumObject-Methode,**](idirectxfile--createenumobject.md) um ein [**IDirectXFileEnumObject-Enumeratorobjekt**](idirectxfileenumobject.md) zu erstellen.
4.  Schleife durch die Objekte in der Datei. Führen Sie für jedes Objekt die folgenden Schritte aus.
    1.  Verwenden Sie [**die IDirectXFileEnumObject::GetNextDataObject-Methode,**](idirectxfileenumobject--getnextdataobject.md) um jedes [**IDirectXFileData-Objekt**](idirectxfiledata.md) abzurufen.
    2.  Verwenden Sie [**die IDirectXFileData::GetType-Methode,**](idirectxfiledata--gettype.md) um den Datentyp der Daten abzurufen.
    3.  Laden Sie die Daten mithilfe der [**IDirectXFileData::GetData-Methode.**](idirectxfiledata--getdata.md)
    4.  Wenn das Objekt über optionale Member verfügt, rufen Sie die optionalen Member ab, indem Sie die [**IDirectXFileData::GetNextObject-Methode**](idirectxfiledata--getnextobject.md) aufrufen.
    5.  Geben Sie das [**IDirectXFileData-Objekt**](idirectxfiledata.md) frei.
5.  Geben Sie das [**IDirectXFileEnumObject-Objekt**](idirectxfileenumobject.md) frei.
6.  Geben Sie das [**IDirectXFile-Objekt**](idirectxfile.md) frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateien (Legacy)](x-files--legacy-.md)
</dt> </dl>

 

 




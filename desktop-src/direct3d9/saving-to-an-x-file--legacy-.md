---
description: Verwenden Sie das folgende Verfahren in Legacyanwendungen, um X-Dateivorlagen und -Daten in einer X-Datei zu speichern.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Speichern in einer X-Datei (Legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03070b25c8839ddd17ab698a4f017822004d027d978b5c4ce589491f2e8fb8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797782"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Speichern in einer X-Datei (Legacy) (Direct3D 9)

Verwenden Sie das folgende Verfahren in Legacyanwendungen, um X-Dateivorlagen und -Daten in einer X-Datei zu speichern.

1.  Verwenden Sie die [**DirectXFileCreate-Funktion,**](directxfilecreate.md) um ein [**IDirectXFile-Objekt**](idirectxfile.md) zu erstellen.
2.  Verwenden Sie die [**IDirectXFile::RegisterTemplates-Methode,**](idirectxfile--registertemplates.md) um das DirectX-Dateisystem über alle Vorlagen zu informieren, die Sie verwenden werden.
3.  Verwenden Sie die [**IDirectXFile::CreateSaveObject-Methode,**](idirectxfile--createsaveobject.md) um ein [**IDirectXFileSaveObject-Objekt**](idirectxfilesaveobject.md) zu erstellen.
4.  Verwenden Sie bei Bedarf die [**IDirectXFileSaveObject::SaveTemplates-Methode,**](idirectxfilesaveobject--savetemplates.md) um Vorlagen zu speichern.
5.  Durchlaufen Sie die zu speichernde Objekte. Führen Sie für jedes Objekt der obersten Ebene die folgenden Schritte aus.
    -   Verwenden Sie die [**IDirectXFileSaveObject::CreateDataObject-Methode,**](idirectxfilesaveobject--createdataobject.md) um ein [**IDirectXFileData-Objekt**](idirectxfiledata.md) als Objekt der obersten Ebene in der Datei zu erstellen. Wenn das Datenobjekt der obersten Ebene über optionale untergeordnete Objekte verfügt, fügen Sie sie dem -Objekt hinzu, indem Sie die entsprechende -Methode aus dem nächsten Schritt verwenden.
    -   Jedes [**IDirectXFileData-Objekt**](idirectxfiledata.md) kann optionale untergeordnete Objekte aufweisen, wenn die Vorlage dies zulässt. Die untergeordneten Objekte können beliebige der drei Objekttypen sein: **IDirectXFileData,** [**IDirectXFileDataReference**](idirectxfiledatareference.md)oder [**IDirectXFileBinary.**](idirectxfilebinary.md) Durchlaufen Sie die objekte, die Sie speichern müssen, und fügen Sie der Objektliste die einzelnen optionalen untergeordneten Member entsprechend ihrem Typ hinzu, wie in den folgenden Schritten veranschaulicht. Wenn der Objekttyp Data lautet, rufen Sie dann die [**IDirectXFileSaveObject::CreateDataObject-Methode**](idirectxfilesaveobject--createdataobject.md) auf, um ein **IDirectXFileData-Objekt** zu erstellen, und rufen Sie dann die [**IDirectXFileData::AddDataObject-Methode**](idirectxfiledata--adddataobject.md) auf, um es als untergeordnetes Element des Objekts hinzuzufügen. Wenn der Objekttyp Datenverweis ist, rufen Sie die [**IDirectXFileData::AddDataReference-Methode**](idirectxfiledata--adddatareference.md) auf, um das Datenverweisobjekt als untergeordnetes Element des Objekts zu erstellen und hinzuzufügen. Wenn der Objekttyp Binary ist, rufen Sie die [**IDirectXFileData::AddBinaryObject-Methode**](idirectxfiledata--addbinaryobject.md) auf, um das binäre Objekt als untergeordnetes Objekt des Objekts zu erstellen und hinzuzufügen.
    -   Rufen Sie die [**IDirectXFileSaveObject::SaveData-Methode**](idirectxfilesaveobject--savedata.md) auf, um das Datenobjekt und seine untergeordneten Elemente zu speichern.
    -   Geben Sie das [**IDirectXFileData-Objekt**](idirectxfiledata.md) frei.
6.  Geben Sie das [**IDirectXFileSaveObject-Objekt**](idirectxfilesaveobject.md) frei.
7.  Geben Sie das [**IDirectXFile-Objekt**](idirectxfile.md) frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateien (Legacy)](x-files--legacy-.md)
</dt> </dl>

 

 




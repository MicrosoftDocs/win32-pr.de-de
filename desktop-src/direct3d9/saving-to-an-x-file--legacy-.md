---
description: Verwenden Sie das folgende Verfahren in Legacy Anwendungen, um x-Datei Vorlagen und-Daten in einer x-Datei zu speichern.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Speichern in einer X-Datei (Legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f824c8e3ab9cd360a93d3f69fd1a2352548ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341698"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Speichern in einer X-Datei (Legacy) (Direct3D 9)

Verwenden Sie das folgende Verfahren in Legacy Anwendungen, um x-Datei Vorlagen und-Daten in einer x-Datei zu speichern.

1.  Verwenden Sie die Funktion [**directxfilecreate**](directxfilecreate.md) zum Erstellen eines [**idirectxfile**](idirectxfile.md) -Objekts.
2.  Verwenden Sie die [**idirectxfile:: registertemplates**](idirectxfile--registertemplates.md) -Methode, um das DirectX-Dateisystem über alle Vorlagen zu informieren, die Sie verwenden werden.
3.  Verwenden Sie die [**idirectxfile:: kreatesaveobject**](idirectxfile--createsaveobject.md) -Methode, um ein [**idirectxfilesaveobject**](idirectxfilesaveobject.md) -Objekt zu erstellen.
4.  Verwenden Sie die [**idirectxfilesaveobject:: savetemplates**](idirectxfilesaveobject--savetemplates.md) -Methode, um Vorlagen zu speichern, wenn gewünscht.
5.  Durchlaufen Sie die zu speichernden Objekte. Führen Sie für jedes Objekt der obersten Ebene die folgenden Schritte aus.
    -   Verwenden Sie die [**idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md) -Methode, um ein [**idirectxfiledata**](idirectxfiledata.md) -Objekt als Objekt der obersten Ebene in der Datei zu erstellen. Wenn das Datenobjekt der obersten Ebene optionale untergeordnete Objekte aufweist, fügen Sie Sie dem-Objekt hinzu, indem Sie die entsprechende-Methode aus dem nächsten Schritt verwenden.
    -   Jedes [**idirectxfiledata**](idirectxfiledata.md) -Objekt kann optionale untergeordnete Objekte haben, wenn seine Vorlage dies zulässt. Bei den untergeordneten Objekten kann es sich um einen beliebigen der drei Objekttypen handeln: **idirectxfiledata**, [**idirectxfiledatareferenzierung**](idirectxfiledatareference.md)oder [**idirectxfilebinary**](idirectxfilebinary.md). Durchlaufen Sie die Objekte, die Sie speichern müssen, und fügen Sie jedes optionale untergeordnete Element der Objektliste entsprechend dem Typ hinzu, wie in den folgenden Schritten veranschaulicht. Wenn der Objekttyp "Daten" ist, rufen Sie dann die [**idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md) -Methode auf, um ein **idirectxfiledata** -Objekt zu erstellen, und rufen Sie dann die [**idirectxfiledata:: adddataobject**](idirectxfiledata--adddataobject.md) -Methode auf, um Sie als untergeordnetes Element des Objekts hinzuzufügen Wenn der Objekttyp Daten Verweis ist, rufen Sie die [**idirectxfiledata:: adddatareferenzierungsmethode**](idirectxfiledata--adddatareference.md) auf, um das Daten Verweis Objekt als untergeordnetes Element des-Objekts zu erstellen und hinzuzufügen. Wenn der Objekttyp binär ist, rufen Sie die [**idirectxfiledata:: addbinaryobject**](idirectxfiledata--addbinaryobject.md) -Methode auf, um das binäre Objekt als untergeordnetes Element des-Objekts zu erstellen und hinzuzufügen.
    -   Ruft die [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md) -Methode auf, um das Datenobjekt und seine untergeordneten Elemente zu speichern.
    -   Geben Sie das [**idirectxfiledata**](idirectxfiledata.md) -Objekt frei.
6.  Geben Sie das [**idirectxfilesaveobject**](idirectxfilesaveobject.md) -Objekt frei.
7.  Geben Sie das [**idirectxfile**](idirectxfile.md) -Objekt frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateien (Legacy)](x-files--legacy-.md)
</dt> </dl>

 

 




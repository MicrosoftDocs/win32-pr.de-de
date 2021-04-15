---
description: Verwenden Sie das folgende Verfahren in Legacy Anwendungen, um eine x-Datei zu laden.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Laden einer X-Datei (Legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521168"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Laden einer X-Datei (Legacy) (Direct3D 9)

Verwenden Sie das folgende Verfahren in Legacy Anwendungen, um eine x-Datei zu laden.

1.  Verwenden Sie die Funktion [**directxfilecreate**](directxfilecreate.md) zum Erstellen eines [**idirectxfile**](idirectxfile.md) -Objekts.
2.  Wenn Vorlagen in der DirectX-Datei vorhanden sind, die Sie laden möchten, verwenden Sie die [**idirectxfile:: registertemplates**](idirectxfile--registertemplates.md) -Methode, um diese Vorlagen zu registrieren.
3.  Verwenden Sie die [**idirectxfile:: kreateenumuject**](idirectxfile--createenumobject.md) -Methode, um ein [**idirectxfileenumubject**](idirectxfileenumobject.md) -Enumeratorobjekt zu erstellen.
4.  Durchlaufen Sie die Objekte in der Datei. Führen Sie für jedes-Objekt die folgenden Schritte aus.
    1.  Verwenden Sie die [**idirectxfileenufibject:: getnextdataobject**](idirectxfileenumobject--getnextdataobject.md) -Methode, um die einzelnen [**idirectxfiledata**](idirectxfiledata.md) -Objekte abzurufen.
    2.  Verwenden Sie die [**idirectxfiledata:: GetType**](idirectxfiledata--gettype.md) -Methode, um den Datentyp abzurufen.
    3.  Laden Sie die Daten mithilfe der [**idirectxfiledata:: GetData**](idirectxfiledata--getdata.md) -Methode.
    4.  Wenn das Objekt über optionale Member verfügt, rufen Sie die optionalen Member ab, indem Sie die [**idirectxfiledata:: getnextobject**](idirectxfiledata--getnextobject.md) -Methode aufrufen.
    5.  Geben Sie das [**idirectxfiledata**](idirectxfiledata.md) -Objekt frei.
5.  Geben Sie das [**idirectxfileenumubject**](idirectxfileenumobject.md) -Objekt frei.
6.  Geben Sie das [**idirectxfile**](idirectxfile.md) -Objekt frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateien (Legacy)](x-files--legacy-.md)
</dt> </dl>

 

 




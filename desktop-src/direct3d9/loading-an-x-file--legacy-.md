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
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="3d90c-103">Laden einer X-Datei (Legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3d90c-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="3d90c-104">Verwenden Sie das folgende Verfahren in Legacy Anwendungen, um eine x-Datei zu laden.</span><span class="sxs-lookup"><span data-stu-id="3d90c-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="3d90c-105">Verwenden Sie die Funktion [**directxfilecreate**](directxfilecreate.md) zum Erstellen eines [**idirectxfile**](idirectxfile.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3d90c-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="3d90c-106">Wenn Vorlagen in der DirectX-Datei vorhanden sind, die Sie laden möchten, verwenden Sie die [**idirectxfile:: registertemplates**](idirectxfile--registertemplates.md) -Methode, um diese Vorlagen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="3d90c-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="3d90c-107">Verwenden Sie die [**idirectxfile:: kreateenumuject**](idirectxfile--createenumobject.md) -Methode, um ein [**idirectxfileenumubject**](idirectxfileenumobject.md) -Enumeratorobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d90c-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="3d90c-108">Durchlaufen Sie die Objekte in der Datei.</span><span class="sxs-lookup"><span data-stu-id="3d90c-108">Loop through the objects in the file.</span></span> <span data-ttu-id="3d90c-109">Führen Sie für jedes-Objekt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3d90c-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="3d90c-110">Verwenden Sie die [**idirectxfileenufibject:: getnextdataobject**](idirectxfileenumobject--getnextdataobject.md) -Methode, um die einzelnen [**idirectxfiledata**](idirectxfiledata.md) -Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d90c-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="3d90c-111">Verwenden Sie die [**idirectxfiledata:: GetType**](idirectxfiledata--gettype.md) -Methode, um den Datentyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d90c-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="3d90c-112">Laden Sie die Daten mithilfe der [**idirectxfiledata:: GetData**](idirectxfiledata--getdata.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3d90c-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="3d90c-113">Wenn das Objekt über optionale Member verfügt, rufen Sie die optionalen Member ab, indem Sie die [**idirectxfiledata:: getnextobject**](idirectxfiledata--getnextobject.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3d90c-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="3d90c-114">Geben Sie das [**idirectxfiledata**](idirectxfiledata.md) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="3d90c-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="3d90c-115">Geben Sie das [**idirectxfileenumubject**](idirectxfileenumobject.md) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="3d90c-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="3d90c-116">Geben Sie das [**idirectxfile**](idirectxfile.md) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="3d90c-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d90c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d90c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d90c-118">X-Dateien (Legacy)</span><span class="sxs-lookup"><span data-stu-id="3d90c-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 




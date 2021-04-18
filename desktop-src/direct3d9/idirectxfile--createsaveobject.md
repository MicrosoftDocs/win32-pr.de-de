---
description: Erstellt ein Save-Objekt. Veraltet.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'Idirectxfile:: kreatesaveobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365125"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="c68e4-104">Idirectxfile:: erkreatesaveobject-Methode</span><span class="sxs-lookup"><span data-stu-id="c68e4-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="c68e4-105">Erstellt ein Save-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c68e4-105">Creates a save object.</span></span> <span data-ttu-id="c68e4-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c68e4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c68e4-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="c68e4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68e4-109">*szFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c68e4-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c68e4-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c68e4-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c68e4-111">Zeiger auf den Namen der Datei, die zum Speichern von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c68e4-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="c68e4-112">*dwfileformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c68e4-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c68e4-113">Typ: **[ **dxfileformat**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="c68e4-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="c68e4-114">Gibt das Format an, das beim Speichern der DirectX-Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c68e4-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="c68e4-115">Bei diesem Wert kann es sich um eines der dxfileformat \_ xxx-Flags in [dxfile-Konstanten](dxfile.md)handeln.</span><span class="sxs-lookup"><span data-stu-id="c68e4-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="c68e4-116">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="c68e4-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c68e4-117">*ppsaveobj* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c68e4-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c68e4-118">Typ: **[ **lpdirectxfilesaveobject**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="c68e4-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="c68e4-119">Adresse eines Zeigers auf eine [**idirectxfilesaveobject**](idirectxfilesaveobject.md) -Schnittstelle, die das erstellte Save-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c68e4-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68e4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c68e4-120">Return value</span></span>

<span data-ttu-id="c68e4-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c68e4-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c68e4-122">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="c68e4-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c68e4-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badzuzuweisung, dxfileerr \_ BadFile, dxfileerr \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="c68e4-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68e4-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c68e4-124">Remarks</span></span>

<span data-ttu-id="c68e4-125">Nachdem Sie diese Methode verwendet haben, verwenden Sie die Methoden der [**idirectxfilesaveobject**](idirectxfilesaveobject.md) -Schnittstelle zum Erstellen von Datenobjekten und zum Speichern von Vorlagen oder Daten.</span><span class="sxs-lookup"><span data-stu-id="c68e4-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="c68e4-126">Der Standardwert für das Dateiformat lautet dxfileformat \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="c68e4-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="c68e4-127">Die Dateiformat Werte können mit einem logischen OR kombiniert werden, um komprimierten Text oder komprimierte Binärdateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c68e4-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="c68e4-128">Wenn eine Datei sowohl als Binärdatei (0) als auch als Text (1) angegeben wird, wird Sie als Textdatei gespeichert, da der Wert nicht vom Textdatei-Format Wert (0 + 1 = 1) unterschieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="c68e4-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="c68e4-129">Wenn Sie angeben, dass das Dateiformat Text und Komprimierung sein soll, wird die Datei zunächst als Text geschrieben und dann komprimiert.</span><span class="sxs-lookup"><span data-stu-id="c68e4-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="c68e4-130">Komprimierte Textdateien sind jedoch nicht so effizient wie binäre Textdateien. in den meisten Fällen sollten Sie Binär-und komprimierte Textdateien angeben.</span><span class="sxs-lookup"><span data-stu-id="c68e4-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="c68e4-131">Wenn eine Datei festgelegt wird, die ohne Angabe eines Formats komprimiert werden soll, führt dies zu einer binären komprimierten Datei.</span><span class="sxs-lookup"><span data-stu-id="c68e4-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68e4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c68e4-132">Requirements</span></span>



| <span data-ttu-id="c68e4-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c68e4-133">Requirement</span></span> | <span data-ttu-id="c68e4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c68e4-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c68e4-135">Header</span><span class="sxs-lookup"><span data-stu-id="c68e4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c68e4-136"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c68e4-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c68e4-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c68e4-137">Library</span></span><br/> | <dl> <span data-ttu-id="c68e4-138"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c68e4-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68e4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c68e4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68e4-140">Idirectxfile</span><span class="sxs-lookup"><span data-stu-id="c68e4-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="c68e4-141">**Idirectxfilesaveobject**</span><span class="sxs-lookup"><span data-stu-id="c68e4-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 

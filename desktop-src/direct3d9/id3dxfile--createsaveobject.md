---
description: Erstellt ein Speicher Objekt, das zum Speichern von Daten in einer x-Datei verwendet wird.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile:: kreatesaveobject-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353379"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="dc0b2-103">ID3DXFile:: kreatesaveobject-Methode</span><span class="sxs-lookup"><span data-stu-id="dc0b2-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="dc0b2-104">Erstellt ein Speicher Objekt, das zum Speichern von Daten in einer x-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc0b2-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="dc0b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc0b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0b2-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0b2-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0b2-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc0b2-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc0b2-109">Zeiger auf den Namen der Datei, die zum Speichern von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="dc0b2-110">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0b2-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0b2-111">Type: **[D3DXF \_ filesaveoptions](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="dc0b2-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="dc0b2-112">-Wert, der den Namen der Datei angibt, in der Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="dc0b2-113">Bei diesem Wert kann es sich um eines der Optionen für die [Dateispeicher Optionen](d3dxf.md) handeln.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="dc0b2-114">*dwfileformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0b2-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0b2-115">Type: **[D3DXF \_ File Format](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="dc0b2-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="dc0b2-116">Gibt das Format an, das beim Speichern der x-Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="dc0b2-117">Bei diesem Wert kann es sich um eines der [dateiformatflags](d3dxf.md) handeln.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="dc0b2-118">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dc0b2-119">*ppsaveobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc0b2-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0b2-120">Typ: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc0b2-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="dc0b2-121">Adresse eines Zeigers auf eine [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstelle, die das erstellte Save-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0b2-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc0b2-122">Return value</span></span>

<span data-ttu-id="dc0b2-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc0b2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc0b2-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dc0b2-125">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR Parameter \_ Error.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc0b2-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc0b2-126">Remarks</span></span>

<span data-ttu-id="dc0b2-127">Nachdem Sie diese Methode verwendet haben, verwenden Sie Methoden der [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstelle zum Erstellen von Datenobjekten und zum Speichern von Vorlagen oder Daten.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="dc0b2-128">Im gespeicherten Dateiformat *dwfileformat* muss eines der Binär-, Legacy-oder textflags in [Dateiformaten](d3dxf.md) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="dc0b2-129">Die Datei kann mit dem optionalen D3DXF \_ File Format-Flag komprimiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="dc0b2-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="dc0b2-130">Die Dateiformat Werte können mit einem logischen OR kombiniert werden, um komprimierten Text oder komprimierte Binärdateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="dc0b2-131">Wenn Sie angeben, dass das Dateiformat Text und Komprimierung sein soll, wird die Datei zuerst als Text geschrieben und dann komprimiert.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="dc0b2-132">Komprimierte Textdateien sind jedoch nicht so effizient wie binäre Textdateien. in den meisten Fällen ist es daher ratsam, Binär und komprimierte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dc0b2-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0b2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc0b2-133">Requirements</span></span>



| <span data-ttu-id="dc0b2-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc0b2-134">Requirement</span></span> | <span data-ttu-id="dc0b2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="dc0b2-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0b2-136">Header</span><span class="sxs-lookup"><span data-stu-id="dc0b2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="dc0b2-137"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0b2-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="dc0b2-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc0b2-138">Library</span></span><br/> | <dl> <span data-ttu-id="dc0b2-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc0b2-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dc0b2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc0b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0b2-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="dc0b2-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="dc0b2-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="dc0b2-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 

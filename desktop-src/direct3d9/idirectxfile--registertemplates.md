---
description: Registriert benutzerdefinierte Vorlagen. Veraltet.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'Idirectxfile:: registertemplates-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361197"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="2b7e0-104">Idirectxfile:: registertemplates-Methode</span><span class="sxs-lookup"><span data-stu-id="2b7e0-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="2b7e0-105">Registriert benutzerdefinierte Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="2b7e0-105">Registers custom templates.</span></span> <span data-ttu-id="2b7e0-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2b7e0-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7e0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b7e0-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="2b7e0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b7e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b7e0-109">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b7e0-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7e0-110">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b7e0-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b7e0-111">Ein Zeiger auf einen Puffer, der aus einer DirectX-Datei im Text-oder Binärformat besteht, die Vorlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="2b7e0-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="2b7e0-112">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b7e0-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7e0-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b7e0-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b7e0-114">Größe des Puffers, auf den pvData zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="2b7e0-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b7e0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b7e0-115">Return value</span></span>

<span data-ttu-id="2b7e0-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b7e0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b7e0-117">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="2b7e0-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2b7e0-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badfilefloatsize, dxfileerr \_ badfiletype, dxfileerr \_ badfileversion, dxfileerr \_ badvalue, dxfileerr \_ parametererror.</span><span class="sxs-lookup"><span data-stu-id="2b7e0-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b7e0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b7e0-119">Remarks</span></span>

<span data-ttu-id="2b7e0-120">Das folgende Code Fragment stellt einen Beispiel aufzurufen von **Register Templates** und Beispiel Inhalt für den Puffer bereit, in den pvData verweist.</span><span class="sxs-lookup"><span data-stu-id="2b7e0-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="2b7e0-121">Alle Vorlagen müssen einen Namen und einen universell eindeutigen Bezeichner (UUID) angeben.</span><span class="sxs-lookup"><span data-stu-id="2b7e0-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b7e0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b7e0-122">Requirements</span></span>



| <span data-ttu-id="2b7e0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b7e0-123">Requirement</span></span> | <span data-ttu-id="2b7e0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2b7e0-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7e0-125">Header</span><span class="sxs-lookup"><span data-stu-id="2b7e0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2b7e0-126"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b7e0-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b7e0-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b7e0-127">Library</span></span><br/> | <dl> <span data-ttu-id="2b7e0-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b7e0-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b7e0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b7e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7e0-130">Idirectxfile</span><span class="sxs-lookup"><span data-stu-id="2b7e0-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 

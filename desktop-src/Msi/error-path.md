---
description: In Windows Installer Versionen 1,0 und 1,1 ist die Path-Eigenschaft immer die leere Zeichenfolge. In zukünftigen Versionen kann dieser Wert verwendet werden, um den Pfad zur Datei oder zum Verzeichnis zurückzugeben, die nicht erstellt werden konnte.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Error. Path-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365997"
---
# <a name="errorpath-property"></a><span data-ttu-id="cef34-104">Error. Path-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cef34-104">Error.Path property</span></span>

<span data-ttu-id="cef34-105">In Windows Installer Versionen 1,0 und 1,1 ist die Path-Eigenschaft immer die leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cef34-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="cef34-106">In zukünftigen Versionen kann dieser Wert verwendet werden, um den Pfad zur Datei oder zum Verzeichnis zurückzugeben, die nicht erstellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cef34-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="cef34-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cef34-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef34-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cef34-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="cef34-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cef34-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="cef34-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cef34-110">Remarks</span></span>

<span data-ttu-id="cef34-111">Dieser Wert ist nur für Fehler vom Typ msmerrorfilecreate oder msmerrordircreate gültig.</span><span class="sxs-lookup"><span data-stu-id="cef34-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="cef34-112">Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cef34-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="cef34-113">C++</span><span class="sxs-lookup"><span data-stu-id="cef34-113">C++</span></span>

<span data-ttu-id="cef34-114">Siehe [**get \_ path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span><span class="sxs-lookup"><span data-stu-id="cef34-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef34-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cef34-115">Requirements</span></span>



| <span data-ttu-id="cef34-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cef34-116">Requirement</span></span> | <span data-ttu-id="cef34-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cef34-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cef34-118">Version</span><span class="sxs-lookup"><span data-stu-id="cef34-118">Version</span></span><br/> | <span data-ttu-id="cef34-119">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cef34-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="cef34-120">Header</span><span class="sxs-lookup"><span data-stu-id="cef34-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cef34-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="cef34-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="cef34-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cef34-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cef34-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cef34-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 


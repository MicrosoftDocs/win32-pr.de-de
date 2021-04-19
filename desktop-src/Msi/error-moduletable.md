---
description: Die schreibgeschützte moduletable-Eigenschaft gibt den Namen der Tabelle im Modul zurück, das den Fehler verursacht hat.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Error. moduletable-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369620"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="f788e-103">Error. moduletable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f788e-103">Error.ModuleTable property</span></span>

<span data-ttu-id="f788e-104">Die Schreib **geschützte moduletable** -Eigenschaft gibt den Namen der Tabelle im Modul zurück, das den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f788e-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="f788e-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f788e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f788e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f788e-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="f788e-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f788e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f788e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f788e-108">Remarks</span></span>

<span data-ttu-id="f788e-109">Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen.</span><span class="sxs-lookup"><span data-stu-id="f788e-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="f788e-110">Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f788e-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="f788e-111">C++</span><span class="sxs-lookup"><span data-stu-id="f788e-111">C++</span></span>

<span data-ttu-id="f788e-112">Weitere Informationen finden [**Sie unter Get \_ moduletable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span><span class="sxs-lookup"><span data-stu-id="f788e-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f788e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f788e-113">Requirements</span></span>



| <span data-ttu-id="f788e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f788e-114">Requirement</span></span> | <span data-ttu-id="f788e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f788e-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f788e-116">Version</span><span class="sxs-lookup"><span data-stu-id="f788e-116">Version</span></span><br/> | <span data-ttu-id="f788e-117">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f788e-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="f788e-118">Header</span><span class="sxs-lookup"><span data-stu-id="f788e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f788e-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="f788e-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="f788e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f788e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f788e-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f788e-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 


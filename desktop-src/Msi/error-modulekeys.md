---
description: Die schreibgeschützte modulekeys-Eigenschaft des Error-Objekts gibt einen Zeiger auf eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Zeile im Modul enthält, die den Fehler verursacht hat, einen Schlüssel pro Eintrag in der Auflistung.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Error. modulekeys-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360359"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="82210-103">Error. modulekeys (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82210-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="82210-104">Die schreibgeschützte **modulekeys** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt einen Zeiger auf eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Zeile im Modul enthält, die den Fehler verursacht hat, einen Schlüssel pro Eintrag in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="82210-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="82210-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="82210-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82210-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="82210-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="82210-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="82210-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="82210-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82210-108">Remarks</span></span>

<span data-ttu-id="82210-109">Der Client ist für das Freigeben der Zeichen folgen Auflistung verantwortlich, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="82210-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="82210-110">Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen.</span><span class="sxs-lookup"><span data-stu-id="82210-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="82210-111">Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="82210-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="82210-112">C++</span><span class="sxs-lookup"><span data-stu-id="82210-112">C++</span></span>

<span data-ttu-id="82210-113">Weitere Informationen finden [**Sie unter Get \_ modulekeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span><span class="sxs-lookup"><span data-stu-id="82210-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="82210-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82210-114">Requirements</span></span>



| <span data-ttu-id="82210-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82210-115">Requirement</span></span> | <span data-ttu-id="82210-116">Wert</span><span class="sxs-lookup"><span data-stu-id="82210-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82210-117">Version</span><span class="sxs-lookup"><span data-stu-id="82210-117">Version</span></span><br/> | <span data-ttu-id="82210-118">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="82210-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="82210-119">Header</span><span class="sxs-lookup"><span data-stu-id="82210-119">Header</span></span><br/>  | <dl> <span data-ttu-id="82210-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="82210-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="82210-121">DLL</span><span class="sxs-lookup"><span data-stu-id="82210-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="82210-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82210-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 


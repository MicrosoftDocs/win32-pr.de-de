---
description: Die schreibgeschützte databasekeys-Eigenschaft des Error-Objekts gibt eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Datenbankzeile enthält, die den Fehler verursacht hat. In der Sammlung ist ein Schlüssel pro Eintrag vorhanden.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Error. databasekeys-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373576"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="b529e-104">Error. databasekeys (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b529e-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="b529e-105">Die schreibgeschützte **databasekeys** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt eine Zeichen folgen Auflistung zurück, die die Primärschlüssel der Datenbankzeile enthält, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="b529e-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="b529e-106">In der Sammlung ist ein Schlüssel pro Eintrag vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b529e-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="b529e-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b529e-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b529e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b529e-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="b529e-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b529e-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b529e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b529e-110">Remarks</span></span>

<span data-ttu-id="b529e-111">Der Client ist für das Freigeben der Zeichen folgen Auflistung verantwortlich, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b529e-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="b529e-112">Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen.</span><span class="sxs-lookup"><span data-stu-id="b529e-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="b529e-113">Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b529e-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="b529e-114">C++</span><span class="sxs-lookup"><span data-stu-id="b529e-114">C++</span></span>

<span data-ttu-id="b529e-115">Weitere Informationen finden [**Sie unter Get \_ databasekeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span><span class="sxs-lookup"><span data-stu-id="b529e-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b529e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b529e-116">Requirements</span></span>



| <span data-ttu-id="b529e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b529e-117">Requirement</span></span> | <span data-ttu-id="b529e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b529e-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b529e-119">Version</span><span class="sxs-lookup"><span data-stu-id="b529e-119">Version</span></span><br/> | <span data-ttu-id="b529e-120">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b529e-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b529e-121">Header</span><span class="sxs-lookup"><span data-stu-id="b529e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b529e-122"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="b529e-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b529e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b529e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b529e-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b529e-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 


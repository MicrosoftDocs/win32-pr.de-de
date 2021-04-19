---
description: Die schreibgeschützte databasetable-Eigenschaft des Error-Objekts gibt den Namen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Error. databasetable-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369524"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="bbac4-103">Error. databasetable-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bbac4-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="bbac4-104">Die schreibgeschützte **databasetable** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt den Namen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="bbac4-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="bbac4-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bbac4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbac4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbac4-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="bbac4-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bbac4-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bbac4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbac4-108">Remarks</span></span>

<span data-ttu-id="bbac4-109">Die Auflistung ist leer, wenn die Werte nicht auf den Fehlertyp zutreffen.</span><span class="sxs-lookup"><span data-stu-id="bbac4-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="bbac4-110">Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bbac4-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="bbac4-111">C++</span><span class="sxs-lookup"><span data-stu-id="bbac4-111">C++</span></span>

<span data-ttu-id="bbac4-112">Weitere Informationen finden [**Sie unter Get \_ databasetable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span><span class="sxs-lookup"><span data-stu-id="bbac4-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbac4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbac4-113">Requirements</span></span>



| <span data-ttu-id="bbac4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbac4-114">Requirement</span></span> | <span data-ttu-id="bbac4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bbac4-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbac4-116">Version</span><span class="sxs-lookup"><span data-stu-id="bbac4-116">Version</span></span><br/> | <span data-ttu-id="bbac4-117">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bbac4-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="bbac4-118">Header</span><span class="sxs-lookup"><span data-stu-id="bbac4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bbac4-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbac4-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbac4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bbac4-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="bbac4-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbac4-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 


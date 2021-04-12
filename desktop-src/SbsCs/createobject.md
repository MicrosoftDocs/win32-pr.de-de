---
description: Mit der Methode "-Methode" des Microsoft. Windows. ActCtx-Objekts wird ein Objekt im Kontext des aktuellen Manifests erstellt.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. kreateobject-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216545"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="8d741-103">ActCtx. kreateobject-Methode</span><span class="sxs-lookup"><span data-stu-id="8d741-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="8d741-104">Mit **der Methode "** -Methode" des [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) -Objekts wird ein Objekt im Kontext des aktuellen Manifests erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d741-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d741-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d741-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="8d741-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d741-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d741-107">*ObjectID*</span><span class="sxs-lookup"><span data-stu-id="8d741-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="8d741-108">Eine Zeichenfolge, die den Typ des zu erstellenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="8d741-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="8d741-109">Beispielsweise eine COM-ProgID.</span><span class="sxs-lookup"><span data-stu-id="8d741-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d741-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d741-110">Return value</span></span>

<span data-ttu-id="8d741-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8d741-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d741-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d741-112">Requirements</span></span>



| <span data-ttu-id="8d741-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d741-113">Requirement</span></span> | <span data-ttu-id="8d741-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8d741-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d741-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d741-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8d741-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d741-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8d741-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d741-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8d741-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d741-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d741-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8d741-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d741-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d741-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d741-121">IID</span><span class="sxs-lookup"><span data-stu-id="8d741-121">IID</span></span><br/>                      | <span data-ttu-id="8d741-122">IID \_ iactctx ist als 8fa7728f-b69b-4ee5-99f 2-e2aa021bef 28 definiert.</span><span class="sxs-lookup"><span data-stu-id="8d741-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8d741-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d741-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d741-124">**GetObject-Methode**</span><span class="sxs-lookup"><span data-stu-id="8d741-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 





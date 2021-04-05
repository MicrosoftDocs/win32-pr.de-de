---
description: Die GetObject-Methode ruft eine Instanz eines vorhandenen Microsoft. Windows. ActCtx-Objekts ab.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750961"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="de4ab-103">ActCtx. GetObject-Methode</span><span class="sxs-lookup"><span data-stu-id="de4ab-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="de4ab-104">Die **GetObject** -Methode ruft eine Instanz eines vorhandenen [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="de4ab-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de4ab-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="de4ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4ab-107">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="de4ab-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="de4ab-108">Erforderliche Zeichenfolge, die das Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="de4ab-108">Required string that indicates the object.</span></span> <span data-ttu-id="de4ab-109">Der Name muss sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation** befinden.</span><span class="sxs-lookup"><span data-stu-id="de4ab-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4ab-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de4ab-110">Return value</span></span>

<span data-ttu-id="de4ab-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de4ab-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4ab-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de4ab-112">Requirements</span></span>



| <span data-ttu-id="de4ab-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de4ab-113">Requirement</span></span> | <span data-ttu-id="de4ab-114">Wert</span><span class="sxs-lookup"><span data-stu-id="de4ab-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de4ab-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de4ab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="de4ab-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de4ab-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="de4ab-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de4ab-117">Minimum supported server</span></span><br/> | <span data-ttu-id="de4ab-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de4ab-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de4ab-119">DLL</span><span class="sxs-lookup"><span data-stu-id="de4ab-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de4ab-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de4ab-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="de4ab-121">IID</span><span class="sxs-lookup"><span data-stu-id="de4ab-121">IID</span></span><br/>                      | <span data-ttu-id="de4ab-122">IID \_ iactctx ist als 8fa7728f-b69b-4ee5-99f 2-e2aa021bef 28 definiert.</span><span class="sxs-lookup"><span data-stu-id="de4ab-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="de4ab-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de4ab-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4ab-124">**Methode "kreateobject"**</span><span class="sxs-lookup"><span data-stu-id="de4ab-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 





---
description: Stellt den Typ des Pfads dar, der als Argument verwendet wird.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: PATH_TYPE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522952"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="89c08-103">Pfadtyp- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="89c08-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="89c08-104">Stellt den Typ des Pfads dar, der als Argument verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89c08-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="89c08-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="89c08-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="89c08-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="89c08-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS- \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="89c08-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="89c08-108">Standard Pfad.</span><span class="sxs-lookup"><span data-stu-id="89c08-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="89c08-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT- \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="89c08-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="89c08-110">Interner Pfad.</span><span class="sxs-lookup"><span data-stu-id="89c08-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89c08-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89c08-111">Requirements</span></span>



| <span data-ttu-id="89c08-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89c08-112">Requirement</span></span> | <span data-ttu-id="89c08-113">Wert</span><span class="sxs-lookup"><span data-stu-id="89c08-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89c08-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89c08-114">Minimum supported client</span></span><br/> | <span data-ttu-id="89c08-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89c08-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="89c08-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89c08-116">Minimum supported server</span></span><br/> | <span data-ttu-id="89c08-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89c08-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89c08-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89c08-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c08-119">**Sdbkreatedatabase**</span><span class="sxs-lookup"><span data-stu-id="89c08-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="89c08-120">**Sdbopendatabase**</span><span class="sxs-lookup"><span data-stu-id="89c08-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 





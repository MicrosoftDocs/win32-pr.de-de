---
title: WMDM_FIND_SCOPE-Enumeration
description: Der \_ \_ Enumerationstyp für den WMDM-Suchbereich definiert den Gültigkeitsbereich des Speicher Objekts.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- Device Manager der WMDM_FIND_SCOPE-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373620"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="a0ad7-104">WMDM \_ - \_ Enumeration zum Suchen des Bereichs</span><span class="sxs-lookup"><span data-stu-id="a0ad7-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="a0ad7-105">Der Enumerationstyp für den **WMDM- \_ \_ Suchbereich** definiert den Gültigkeitsbereich des Speicher Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0ad7-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ad7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0ad7-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="a0ad7-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a0ad7-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a0ad7-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM-Such \_ \_ Bereich \_ Global**</span><span class="sxs-lookup"><span data-stu-id="a0ad7-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="a0ad7-109">Suchen nach dem passenden Objekt an beliebiger Stelle auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="a0ad7-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="a0ad7-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM-Such \_ \_ Bereich \_ direkt \_ untergeordnete Elemente**</span><span class="sxs-lookup"><span data-stu-id="a0ad7-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="a0ad7-111">Suchen nach dem entsprechenden Objekt innerhalb dieses Speichers und seiner untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0ad7-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0ad7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0ad7-112">Requirements</span></span>



| <span data-ttu-id="a0ad7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0ad7-113">Requirement</span></span> | <span data-ttu-id="a0ad7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ad7-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ad7-115">Header</span><span class="sxs-lookup"><span data-stu-id="a0ad7-115">Header</span></span><br/> | <dl> <span data-ttu-id="a0ad7-116"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0ad7-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ad7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0ad7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ad7-118">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="a0ad7-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 






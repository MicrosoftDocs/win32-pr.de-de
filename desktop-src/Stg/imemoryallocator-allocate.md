---
title: Imemoryallocator-Zuordnungs Methode
description: Die Zuordnungs Methode belegt Arbeitsspeicher für die stgconvertpropertytovariant-Funktion, wenn die Funktion einen serializedpropertyvalue-Datentyp in einen PROPVARIANT-Datentyp konvertiert.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Zuordnen von strukturiertem Speicher
- Zuordnen von strukturiertem Speicher, imemoryallocator-Schnittstelle
- Strukturierter Speicher der imemoryallocator-Schnittstelle, Methode zuordnen
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339929"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="b4fea-106">Imemoryallocator:: Zuordnungs Methode</span><span class="sxs-lookup"><span data-stu-id="b4fea-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="b4fea-107">Die **Zuordnungs Methode belegt** Arbeitsspeicher für die [**stgconvertpropertytovariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion, wenn die Funktion einen **serializedpropertyvalue** -Datentyp in einen **PROPVARIANT** -Datentyp konvertiert.</span><span class="sxs-lookup"><span data-stu-id="b4fea-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4fea-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="b4fea-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4fea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4fea-110">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4fea-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4fea-111">Gibt die Größe des zugeordneten Arbeitsspeichers an.</span><span class="sxs-lookup"><span data-stu-id="b4fea-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4fea-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4fea-112">Requirements</span></span>



| <span data-ttu-id="b4fea-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4fea-113">Requirement</span></span> | <span data-ttu-id="b4fea-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b4fea-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fea-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4fea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fea-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4fea-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b4fea-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4fea-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fea-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4fea-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b4fea-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4fea-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4fea-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4fea-120"><dt>Ole32.lib</dt></span></span> </dl> |



 


---
title: RPC_IF_HANDLE (rpcdce. h)
description: Der RPC \_ - \_ Datentyp "if-Handle" deklariert ein Schnittstellen handle.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956932"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="a8871-104">RPC- \_ if- \_ handle</span><span class="sxs-lookup"><span data-stu-id="a8871-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="a8871-105">Der RPC-Datentyp " **\_ if- \_ handle** " deklariert ein Schnittstellen handle.</span><span class="sxs-lookup"><span data-stu-id="a8871-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="a8871-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8871-106">Remarks</span></span>

<span data-ttu-id="a8871-107">Die RPC-Lauf Zeit Bibliothek verwendet Schnittstellen Handles für den Zugriff auf die Schnittstellen Spezifikations Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="a8871-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="a8871-108">Der mittlerer l-Compiler erstellt automatisch eine Schnittstellen Spezifikations Datenstruktur aus jeder IDL-Datei und erstellt eine globale Variable des Typs RPC \_ if \_ Handle für die Schnittstellen Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="a8871-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="a8871-109">Der mittlerer l-Compiler enthält ein Schnittstellen Handle in jeder für die Schnittstelle generierten Header Datei.</span><span class="sxs-lookup"><span data-stu-id="a8871-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="a8871-110">Funktionen, die die Schnittstellen Spezifikation als Parameter erfordern, zeigen den Datentyp **RPC \_ if \_ handle** an.</span><span class="sxs-lookup"><span data-stu-id="a8871-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="a8871-111">Die Form jedes Schnittstellen handle-namens lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a8871-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="a8871-112">*if-Name* \_ Clientithhandle (für den Client)</span><span class="sxs-lookup"><span data-stu-id="a8871-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="a8871-113">*if-Name* \_ Serverib handle (für den Server)</span><span class="sxs-lookup"><span data-stu-id="a8871-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="a8871-114">Der *if-Name-* Teil gibt den Schnittstellen Bezeichner in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="a8871-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="a8871-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a8871-115">For example:</span></span>

<span data-ttu-id="a8871-116">Hello \_ clientif handle</span><span class="sxs-lookup"><span data-stu-id="a8871-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="a8871-117">Hello \_ serverif handle</span><span class="sxs-lookup"><span data-stu-id="a8871-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="a8871-118">Die maximale Länge des Schnittstellen handle-namens beträgt 31 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a8871-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="a8871-119">Da der " \_ clientibhandle"-und " \_ serveribhandle"-Teil der Namen 15 Zeichen erfordert, darf das *if-Name-* Element höchstens 16 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="a8871-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8871-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8871-120">Requirements</span></span>



| <span data-ttu-id="a8871-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8871-121">Requirement</span></span> | <span data-ttu-id="a8871-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a8871-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8871-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8871-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a8871-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8871-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a8871-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8871-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a8871-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8871-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8871-127">Header</span><span class="sxs-lookup"><span data-stu-id="a8871-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8871-128"><dt>Rpcdce. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8871-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 






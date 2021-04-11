---
title: DNS-Datentypen (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Weitere Informationen finden Sie unter: DNS-Datentypen'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216039"
---
# <a name="dns-data-types"></a><span data-ttu-id="e7b57-104">DNS-Datentypen</span><span class="sxs-lookup"><span data-stu-id="e7b57-104">DNS Data Types</span></span>

<span data-ttu-id="e7b57-105">Die folgenden Datentypen sind für DNS definiert:</span><span class="sxs-lookup"><span data-stu-id="e7b57-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="e7b57-106">**IP4- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="e7b57-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="e7b57-107">Ein-Wert, der eine IPv4-Adresse (Internet Protocol Version 4) darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7b57-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="e7b57-108">Die gepunktete Dezimal-IPv4-Adresse **127.0.0.1** wird z. b. in der Host-Byte-Reihenfolge als **0x7b000001** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e7b57-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7b57-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7b57-109">Requirements</span></span>



| <span data-ttu-id="e7b57-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7b57-110">Requirement</span></span> | <span data-ttu-id="e7b57-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e7b57-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b57-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7b57-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b57-113">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7b57-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e7b57-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7b57-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b57-115">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7b57-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e7b57-116">Header</span><span class="sxs-lookup"><span data-stu-id="e7b57-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b57-117"><dt>Windns. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b57-117"><dt>Windns.h</dt></span></span> </dl> |



 

 






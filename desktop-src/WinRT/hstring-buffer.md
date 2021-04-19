---
description: Ein Handle für einen änderbaren Zeichen folgen Puffer, der zum Erstellen eines hstring verwendet werden kann.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348185"
---
# <a name="hstring_buffer"></a><span data-ttu-id="c6e86-103">hstring- \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="c6e86-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="c6e86-104">Ein Handle für einen änderbaren Zeichen folgen Puffer, der zum Erstellen eines [**hstring**](hstring.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6e86-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="c6e86-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6e86-105">Remarks</span></span>

<span data-ttu-id="c6e86-106">**Hstring \_ Buffer** stellt einen Zeichen folgen Puffer dar, den Sie ändern können, bevor Sie ihn in einen unveränderlichen [**hstring**](hstring.md)-Wert umrechnen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="c6e86-107">Rufen Sie die [**windowshalzugecatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) -Funktion auf, um einen **hstring- \_ Puffer** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="c6e86-108">Ruft den [**windowspromotestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) auf, um einen **hstring- \_ Puffer** in einen unveränderlichen [**hstring**](hstring.md)zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c6e86-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e86-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e86-109">Requirements</span></span>



| <span data-ttu-id="c6e86-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6e86-110">Requirement</span></span> | <span data-ttu-id="c6e86-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c6e86-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e86-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6e86-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e86-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6e86-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="c6e86-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6e86-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e86-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6e86-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c6e86-116">Header</span><span class="sxs-lookup"><span data-stu-id="c6e86-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e86-117"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e86-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e86-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6e86-118">See also</span></span>

<dl> <span data-ttu-id="c6e86-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c6e86-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c6e86-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="c6e86-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="c6e86-121">**Windowshalzugecatestringbuffer**</span><span class="sxs-lookup"><span data-stu-id="c6e86-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="c6e86-122">**Windowspromotestringbuffer**</span><span class="sxs-lookup"><span data-stu-id="c6e86-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 

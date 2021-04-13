---
description: Die "SCard \_ IO Request"- \_ Struktur beginnt mit einer Protokoll Steuerungs Informationsstruktur.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: SCARD_IO_REQUEST Struktur (winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345319"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="68a18-103">SCard \_ IO- \_ Anforderungs Struktur</span><span class="sxs-lookup"><span data-stu-id="68a18-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="68a18-104">Die " **SCard \_ IO \_ Request** "-Struktur beginnt mit einer Protokoll Steuerungs Informationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="68a18-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="68a18-105">Alle Protokoll spezifischen Informationen folgen dann direkt dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="68a18-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="68a18-106">Die gesamte Länge der Struktur muss an der zugrunde liegenden Größe des Hardwarearchitektur Worts ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="68a18-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="68a18-107">In Win32 muss die Länge aller PCI-Informationen z. b. ein Vielfaches von vier Bytes sein, damit Sie sich an einer 32-Bit-Grenze anpasst.</span><span class="sxs-lookup"><span data-stu-id="68a18-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a18-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="68a18-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="68a18-109">Member</span><span class="sxs-lookup"><span data-stu-id="68a18-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="68a18-110">**dwprotocol**</span><span class="sxs-lookup"><span data-stu-id="68a18-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="68a18-111">Das verwendete Protokoll.</span><span class="sxs-lookup"><span data-stu-id="68a18-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="68a18-112">**cbpcilength**</span><span class="sxs-lookup"><span data-stu-id="68a18-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="68a18-113">Länge (in Byte) der Anforderungs-e/a- **\_ \_ Anforderungs** Struktur zuzüglich der folgenden PCI-spezifischen Informationen.</span><span class="sxs-lookup"><span data-stu-id="68a18-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68a18-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68a18-114">Requirements</span></span>



| <span data-ttu-id="68a18-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68a18-115">Requirement</span></span> | <span data-ttu-id="68a18-116">Wert</span><span class="sxs-lookup"><span data-stu-id="68a18-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68a18-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68a18-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68a18-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68a18-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="68a18-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68a18-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68a18-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68a18-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68a18-121">Header</span><span class="sxs-lookup"><span data-stu-id="68a18-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a18-122"><dt>Winsmcrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a18-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a18-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68a18-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a18-124">**Scardüberträgt**</span><span class="sxs-lookup"><span data-stu-id="68a18-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 





---
title: midl_pragma Warning-Attribut
description: Verwenden Sie die Option "Mittell \_ -pragma-Warnung", um das Verhalten für die Warnmeldung von mittlerer l zur Kompilierzeit vorübergehend
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma Warning-Attribut, Mittel l
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857224"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="1c6f8-104">Mittel l- \_ pragma-Warnungs Attribut</span><span class="sxs-lookup"><span data-stu-id="1c6f8-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="1c6f8-105">Verwenden Sie die Option " **Mittell- \_ pragma-Warnung** ", um das Verhalten für die Warnmeldung von mittlerer l zur Kompilierzeit vorübergehend</span><span class="sxs-lookup"><span data-stu-id="1c6f8-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="1c6f8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c6f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6f8-107">*Option "Warnung" \_*</span><span class="sxs-lookup"><span data-stu-id="1c6f8-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="1c6f8-108">Die Option "Warnung" kann eines der folgenden sein: "deaktivieren", "aktivieren", "Standard".</span><span class="sxs-lookup"><span data-stu-id="1c6f8-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f8-109">*Nachrichten \_ Liste*</span><span class="sxs-lookup"><span data-stu-id="1c6f8-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="1c6f8-110">Eine durch Leerzeichen getrennte Liste von Nachrichtennummern.</span><span class="sxs-lookup"><span data-stu-id="1c6f8-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c6f8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c6f8-111">Remarks</span></span>

<span data-ttu-id="1c6f8-112">Das Pragma kann wie ein C-Compiler-Pragma verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c6f8-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="1c6f8-113">Das heißt, dass Sie das Standardverhalten für eine bestimmte Mittell-Warnung deaktiviert, aktiviert oder zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1c6f8-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="1c6f8-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c6f8-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="1c6f8-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c6f8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6f8-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="1c6f8-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 





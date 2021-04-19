---
title: TF_RENDERINGMARKUP Struktur
description: Die TF \_ renderingmarkup-Struktur Struktur enthält einen Bereich und die Informationen zum Anzeige Attribut.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP Struktur-Text Dienst-Framework
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342314"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="a2eec-104">TF \_ renderingmarkup-Struktur</span><span class="sxs-lookup"><span data-stu-id="a2eec-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="a2eec-105">Die [**tf \_ renderingmarkup**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) -Struktur Struktur enthält einen Bereich und die Informationen zum Anzeige Attribut.</span><span class="sxs-lookup"><span data-stu-id="a2eec-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2eec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2eec-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="a2eec-107">Member</span><span class="sxs-lookup"><span data-stu-id="a2eec-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2eec-108">**Prange**</span><span class="sxs-lookup"><span data-stu-id="a2eec-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="a2eec-109">Ein Zeiger auf eine [itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a2eec-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a2eec-110">**tfdisplayattr**</span><span class="sxs-lookup"><span data-stu-id="a2eec-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="a2eec-111">Attributinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a2eec-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2eec-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2eec-112">Remarks</span></span>

<span data-ttu-id="a2eec-113">Diese Struktur befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="a2eec-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="a2eec-114">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="a2eec-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 





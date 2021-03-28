---
UID: NF:ntw.EtwEventUnregister
title: Etweventunregister-Funktion
description: Hebt die Registrierung eines Ereignisses auf.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e61de5aa1c050aedd2c82dec471765baa7e6cdd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101578"
---
# <a name="etweventunregister-function"></a><span data-ttu-id="a91c4-103">Etweventunregister-Funktion</span><span class="sxs-lookup"><span data-stu-id="a91c4-103">EtwEventUnregister function</span></span>


## <a name="description"></a><span data-ttu-id="a91c4-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a91c4-104">Description</span></span>


<span data-ttu-id="a91c4-105"><b>Etweventunregister</b> hebt die Registrierung eines Ereignisses auf.</span><span class="sxs-lookup"><span data-stu-id="a91c4-105">The <b>EtwEventUnregister</b> unregisters an event.</span></span>
            

<span data-ttu-id="a91c4-106">Anbieter können diese Funktion nur über Ihre <a href="/windows/desktop/ETW/controlcallback">controlcallback</a> -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="a91c4-106">Providers can only call this function from their <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> function.</span></span>


## <a name="parameters"></a><span data-ttu-id="a91c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a91c4-107">Parameters</span></span>




### <a name="reghandle-in"></a><span data-ttu-id="a91c4-108">Reghandle [in]</span><span class="sxs-lookup"><span data-stu-id="a91c4-108">RegHandle [in]</span></span>

<span data-ttu-id="a91c4-109">Handle für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a91c4-109">Handle to an event.</span></span>


## <a name="returns"></a><span data-ttu-id="a91c4-110">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="a91c4-110">Returns</span></span>



<span data-ttu-id="a91c4-111">Gibt ein HRESULT zurück.</span><span class="sxs-lookup"><span data-stu-id="a91c4-111">Returns an HRESULT.</span></span>





## <a name="remarks"></a><span data-ttu-id="a91c4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a91c4-112">Remarks</span></span>



## <a name="see-also"></a><span data-ttu-id="a91c4-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a91c4-113">See also</span></span>
---
description: Das caudiorenderterminal-Terminal wird von csinglefilterterminal abgeleitet und implementiert ein statisches audioenderterminal für Wave-Geräte, das den DirectShow-waveout-Filter verwendet. Die meisten MSPs müssen die Implementierung dieses Terminals nicht außer Kraft setzen.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: Caudiorenderterminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364057"
---
# <a name="caudiorenderterminal"></a><span data-ttu-id="0b8fb-104">Caudiorenderterminal</span><span class="sxs-lookup"><span data-stu-id="0b8fb-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="0b8fb-105">Das **caudiorenderterminal** -Terminal wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches audioenderterminal für Wave-Geräte, das den DirectShow-waveout-Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b8fb-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="0b8fb-106">Die meisten MSPs müssen die Implementierung dieses Terminals nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="0b8fb-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="0b8fb-107">Definiert in "msptrmar. h".</span><span class="sxs-lookup"><span data-stu-id="0b8fb-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b8fb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b8fb-108">Remarks</span></span>

<span data-ttu-id="0b8fb-109">Die **caudiorenderterminal** -Methoden zum Festlegen des Lasten [**\_ Ausgleichs**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) und des [**get- \_ Ausgleichs**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) sind nicht implementiert und geben E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="0b8fb-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 




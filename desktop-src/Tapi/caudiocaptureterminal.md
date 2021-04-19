---
description: Das caudiocaptureterminal-Terminal wird von csinglefilterterminal abgeleitet und implementiert mithilfe des DirectShow WaveIn-Filters ein statisches audioerfassungs-Terminal für Wave-Geräte. Die meisten MSPs müssen die Implementierung dieses Terminals nicht außer Kraft setzen.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: Caudiocaptureterminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373154"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="b0e08-104">Caudiocaptureterminal</span><span class="sxs-lookup"><span data-stu-id="b0e08-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="b0e08-105">Das **caudiocaptureterminal** -Terminal wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert mithilfe des DirectShow WaveIn-Filters ein statisches audioerfassungs-Terminal für Wave-Geräte.</span><span class="sxs-lookup"><span data-stu-id="b0e08-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="b0e08-106">Die meisten MSPs müssen die Implementierung dieses Terminals nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="b0e08-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="b0e08-107">Definiert in "msptmac. h".</span><span class="sxs-lookup"><span data-stu-id="b0e08-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e08-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0e08-108">Remarks</span></span>

<span data-ttu-id="b0e08-109">Die " [**Put \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) "-und " [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) "-Methoden von **caudiocaptureterminal** sind nicht implementiert und geben "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e08-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 




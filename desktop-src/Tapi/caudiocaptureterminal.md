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
# <a name="caudiocaptureterminal"></a>Caudiocaptureterminal

Das **caudiocaptureterminal** -Terminal wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert mithilfe des DirectShow WaveIn-Filters ein statisches audioerfassungs-Terminal für Wave-Geräte. Die meisten MSPs müssen die Implementierung dieses Terminals nicht außer Kraft setzen.

Definiert in "msptmac. h".

## <a name="remarks"></a>Bemerkungen

Die " [**Put \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) "-und " [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) "-Methoden von **caudiocaptureterminal** sind nicht implementiert und geben "E \_ notimpl" zurück.

 

 




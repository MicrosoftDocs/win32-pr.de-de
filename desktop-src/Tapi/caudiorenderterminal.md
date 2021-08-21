---
description: Das Terminal CAudioRenderTerminal wird von CSingleFilterTerminal abgeleitet und implementiert ein statisches Audiorenderingterminal für Wellengeräte mithilfe des DirectShow Waveout-Filters. Die meisten MSPs müssen die Implementierung dieses Terminals nicht überschreiben.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1baaa4a2d1e5d7bbe3b72de19de8593be8976ed662e27595dccea4b7432daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869815"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

Das **Terminal CAudioRenderTerminal** wird von [CSingleFilterTerminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches Audiorenderingterminal für Wellengeräte mithilfe des DirectShow Waveout-Filters. Die meisten MSPs müssen die Implementierung dieses Terminals nicht überschreiben.

Definiert in MSPtrmar.h.

## <a name="remarks"></a>Hinweise

Die [**Put \_ Balance-**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) [**und get \_ Balance-Methoden**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) von **CAudioRenderTerminal** sind nicht implementiert und geben E \_ NOTIMPL zurück.

 

 




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
# <a name="caudiorenderterminal"></a>Caudiorenderterminal

Das **caudiorenderterminal** -Terminal wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches audioenderterminal für Wave-Geräte, das den DirectShow-waveout-Filter verwendet. Die meisten MSPs müssen die Implementierung dieses Terminals nicht außer Kraft setzen.

Definiert in "msptrmar. h".

## <a name="remarks"></a>Bemerkungen

Die **caudiorenderterminal** -Methoden zum Festlegen des Lasten [**\_ Ausgleichs**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) und des [**get- \_ Ausgleichs**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) sind nicht implementiert und geben E \_ notimpl zurück.

 

 




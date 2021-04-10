---
title: Transportparametersupdate-Ereignis
description: Tritt auf, wenn eine beliebige Anzahl von Transport Parametern auf der DMR aktualisiert wird.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- Transportparametersupdate-Ereignis Medien-Streaming-API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858232"
---
# <a name="transportparametersupdate-event"></a>Transportparametersupdate-Ereignis

Tritt auf, wenn eine beliebige Anzahl von Transport Parametern auf der DMR aktualisiert wird.

## <a name="syntax"></a>Syntax


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**transportparametersupdatehandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mithilfe der Methode [**Add \_ transportparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) . Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die Methode [**Remove \_ transportparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .

 

 
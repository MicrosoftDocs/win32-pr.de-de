---
title: TransportParametersUpdate-Ereignis
description: Tritt auf, wenn einer der Transportparameter in der DMR aktualisiert wird.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate-EreignisMedienstreaming-API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034518"
---
# <a name="transportparametersupdate-event"></a>TransportParametersUpdate-Ereignis

Tritt auf, wenn einer der Transportparameter in der DMR aktualisiert wird.

## <a name="syntax"></a>Syntax


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um Benachrichtigungen von diesem Ereignis zu verarbeiten, registrieren Sie eine [**TransportParametersUpdateHandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mithilfe der [**add \_ TransportParametersUpdate-Methode.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) Verwenden Sie zum Aufheben der Registrierung des [**Ereignishandlers die remove \_ TransportParametersUpdate-Methode.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)

 

 
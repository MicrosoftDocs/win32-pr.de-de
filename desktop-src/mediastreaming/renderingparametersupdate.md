---
title: Renderingparametersupdate-Ereignis
description: Tritt auf, wenn ein beliebiger Satz von renderingsteuerungsparametern auf der DMR aktualisiert wird.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- Renderingparametersupdate-Ereignis Medien Streaming-API
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314847"
---
# <a name="renderingparametersupdate-event"></a>Renderingparametersupdate-Ereignis

Tritt auf, wenn ein beliebiger Satz von renderingsteuerungsparametern auf der DMR aktualisiert wird.

## <a name="syntax"></a>Syntax


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie mithilfe der [**Add \_ renderingparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) -Methode eine [**renderingparametersupdatehandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) . Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die Methode [**Remove \_ renderingparametersupdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .

 

 
---
title: Connectionstatuschangi-Ereignis
description: Tritt auf, wenn sich der Netzwerk Verbindungsstatus des Geräts ändert.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- Connectionstatuschge-Ereignis Medien-Streaming-API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726761"
---
# <a name="connectionstatuschanged-event"></a>Connectionstatuschangi-Ereignis

Tritt auf, wenn sich der Netzwerk Verbindungsstatus des Geräts ändert.

## <a name="syntax"></a>Syntax


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen von diesem Ereignis zu behandeln, registrieren Sie eine [**connectionstatushandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) mithilfe der [**Add \_ connectionstatuschangi-Methode**](ibasicdevice-add-connectionstatuschanged.md) . Um die Registrierung des Ereignis Handlers aufzuheben, verwenden Sie die Methode [**Remove \_ connectionstatuschangi.**](ibasicdevice-remove-connectionstatuschanged.md)

 

 
---
title: ConnectionStatusChanged-Ereignis
description: Tritt ein, wenn sich der Netzwerkverbindungsstatus des Geräts ändert.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- ConnectionStatusChanged-Ereignis- Medienstreaming-API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060430"
---
# <a name="connectionstatuschanged-event"></a>ConnectionStatusChanged-Ereignis

Tritt ein, wenn sich der Netzwerkverbindungsstatus des Geräts ändert.

## <a name="syntax"></a>Syntax


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um Benachrichtigungen von diesem Ereignis zu verarbeiten, registrieren Sie eine [**ConnectionStatusHandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) mithilfe der [**add \_ ConnectionStatusChanged-Methode.**](ibasicdevice-add-connectionstatuschanged.md) Verwenden Sie zum Aufheben der Registrierung des Ereignishandlers [**die \_ Remove ConnectionStatusChanged-Methode.**](ibasicdevice-remove-connectionstatuschanged.md)

 

 
---
description: Tritt auf, wenn eine Windows Store-App aktiviert wird.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Icoreapplicationview:: aktiviertes Ereignis (Windows. applicationmodel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214606"
---
# <a name="icoreapplicationviewactivated-event"></a>Icoreapplicationview:: aktiviertes Ereignis

Tritt auf, wenn eine Windows Store-App aktiviert wird.

## <a name="syntax"></a>Syntax


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ in\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**Exit**](/previous-versions//hh438368(v=vs.85)) -Methode kann nicht innerhalb des *Handlers* aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                               |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. Core. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. applicationmodel. Core. idl</dt> </dl> |



 

 

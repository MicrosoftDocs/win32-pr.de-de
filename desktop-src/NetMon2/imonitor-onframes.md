---
description: Die OnFrames-Methode muss vom Monitor implementiert werden. McSVC ruft diese Methode auf, wenn entweder der Erfassungspuffer voll ist oder die Aktualisierungszeit verstrichen ist.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: IMonitor::OnFrames-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a4138c35384753c8df79728a61decf78bf302d0dc9c0a71ca9f787d76a70a620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779170"
---
# <a name="imonitoronframes-method"></a>IMonitor::OnFrames-Methode

Die **OnFrames-Methode** muss vom Monitor implementiert werden. McSVC ruft diese Methode auf, wenn entweder der Erfassungspuffer voll ist oder die Aktualisierungszeit verstrichen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ereignis* \[ In\]
</dt> <dd>

[UPDATE \_ EVENT-Struktur,](update-event.md) die Frameinformationen enthält, die zum Aktualisieren von Ereignissen verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert S OK (was mit \_ NOERROR identisch ist). McSVC übergibt den zurückgegebenen Wert zur Verarbeitung zurück an das NPP.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. McSVC übergibt den zurückgegebenen Wert zur Verarbeitung zurück an das NPP.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





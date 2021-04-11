---
description: Die OnStart-Methode ist eine optionale Methode, die vom Monitor implementiert werden kann. Die mcsvc ruft diese Methode auf, um anzufordern, dass der Monitor die Erfassung startet.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Imonitor:: OnStart-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128324"
---
# <a name="imonitoronstart-method"></a>Imonitor:: OnStart-Methode

Die **OnStart** -Methode ist eine optionale Methode, die vom Monitor implementiert werden kann. Die mcsvc ruft diese Methode auf, um anzufordern, dass der Monitor die Erfassung startet.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*punknpp* \[ in\]
</dt> <dd>

Ein [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger auf die [untc](irtc.md) -Schnittstelle. Der Monitor kann diese Schnittstelle verwenden, um Statistiken abzurufen, die verwendet werden können, um zu bestimmen, ob die Erfassung gestartet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError). Wenn S \_ OK zurückgegeben wird, ruft der mcsvc die Methode " [untc:: Start](irtc-start.md) " auf.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Die mcsvc startet die Erfassung nicht, wenn ein Fehlercode zurückgegeben wird.

## <a name="remarks"></a>Bemerkungen

Die mcsvc ruft diese Methode auf, bevor die [untc:: Start](irtc-start.md) -Methode von NPP aufgerufen wird, um die Erfassung zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Imonitor](imonitor.md)
</dt> <dt>

[Netzwerk Paketanbieter](network-packet-providers.md)
</dt> </dl>

 


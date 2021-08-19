---
description: Die DoConfigure-Methode muss vom Monitor implementiert werden. McSVC ruft diese Methode auf, um Konfigurationsinformationen für die Erfassung abzurufen.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: IMonitor::D oConfigure-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 9776ca62cbb61b6708f00d5e1d6d85eeab245b32798683b5afde546d835633c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779190"
---
# <a name="imonitordoconfigure-method"></a>IMonitor::D oConfigure-Methode

Die **DoConfigure-Methode** muss vom Monitor implementiert werden. McSVC ruft diese Methode auf, um Konfigurationsinformationen für die Erfassung abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Name einer Instanz des Monitors.

</dd> <dt>

*pConfiguration* \[ In\]
</dt> <dd>

Von MCSVC bereitgestellte Konfigurationszeichenfolge. Der Monitor muss diese Zeichenfolge für Konfigurationsdaten analysieren.

</dd> <dt>

*ppScriptInstance* \[ out\]
</dt> <dd>

Adresse der HTML-Zeichenfolge, die zum Konfigurieren des Monitors verwendet wird. Wenn ein Standardskript für die Konfiguration verwendet wird, sollte dieser Wert auf **NULL** festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht NOERROR), und der MCSVC führt den Monitor aus.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Der Rückgabewert NMERR \_ MONITOR \_ CONFIG \_ FAILED ist akzeptabel. Wenn dieser Fehler zurückgegeben wird, kann der Monitor jedoch erst gestartet werden, wenn ein zukünftiger **DoConfigure-Aufruf** erfolgreich ist. Jeder andere Fehler verhindert, dass die Instanz des Monitors aktiviert wird.

## <a name="remarks"></a>Hinweise

McSVC ruft diese Methode auf, nachdem eine Verbindung mit dem Netzwerk hergestellt wurde und bevor die [IRTC::Configure-Methode](irtc-configure.md) aufgerufen wird.

Der Monitor kann die von diesem Aufruf bereitgestellten Informationen speichern, das HTML-Skript oder die Konfigurationszeichenfolge aktualisieren und den [Erfassungsfilter](capture-filters.md) im NPP-BLOB festlegen.

McSVC ruft diese Methode möglicherweise mehrmals auf, kann aber nicht aufgerufen werden, während der Monitor Daten erfasst. Beachten Sie, dass jedes Mal, wenn ein [NPP](network-packet-providers.md) eine Erfassung startet, die Verbindung mit dem Netzwerk konfiguriert werden muss. Diese Einschränkung schließt Situationen ein, in denen das NPP die gleiche Erfassung startet und beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





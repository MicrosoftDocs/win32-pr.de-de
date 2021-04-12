---
description: Die doconfigure-Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, um Konfigurationsinformationen für die Erfassung zu erhalten.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: Imonitor::D oconfigure-Methode (Netmon. h)
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
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128916"
---
# <a name="imonitordoconfigure-method"></a>Imonitor::D oconfigure-Methode

Die **doconfigure** -Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, um Konfigurationsinformationen für die Erfassung zu erhalten.

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

*PName* \[ in\]
</dt> <dd>

Der Name einer Instanz des Monitors.

</dd> <dt>

*pconfiguration* \[ in\]
</dt> <dd>

Konfigurations Zeichenfolge, die von mcsvc bereitgestellt wird. Der Monitor muss diese Zeichenfolge für Konfigurationsdaten analysieren.

</dd> <dt>

*ppscriptinstance* \[ vorgenommen\]
</dt> <dd>

Adresse der HTML-Zeichenfolge, die zum Konfigurieren des Monitors verwendet wird. Wenn ein Standardskript für die Konfiguration verwendet wird, sollte dieser Wert auf **null** festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError), und der mcsvc führt den Monitor aus.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Der Rückgabewert der nmerr- \_ Monitor \_ Konfiguration \_ ist fehlgeschlagen, aber wenn dieser Fehler zurückgegeben wird, kann der Monitor erst gestartet werden, wenn ein zukünftiger **doconfigure** -Rückruf erfolgreich ausgeführt wurde. Jeder andere Fehler verhindert, dass die Instanz des Monitors aktiviert wird.

## <a name="remarks"></a>Bemerkungen

Die mcsvc ruft diese Methode auf, nachdem Sie eine Verbindung mit dem Netzwerk hergestellt hat und bevor die Methode " [iritc:: Configure](irtc-configure.md) " aufgerufen wird.

Der Monitor kann die von diesem-Befehl bereitgestellten Informationen speichern, das HTML-Skript oder die Konfigurations Zeichenfolge aktualisieren und den [Erfassungs Filter](capture-filters.md) im NPP-BLOB festlegen.

Die mcsvc kann diese Methode mehrmals aufrufen, aber Sie kann nicht aufgerufen werden, während der Monitor Daten erfasst. Beachten Sie, dass jedes Mal, wenn eine [NPP](network-packet-providers.md) eine Erfassung startet, die Verbindung mit dem Netzwerk konfiguriert werden muss. Diese Einschränkung umfasst Situationen, in denen die NPP die gleiche Erfassung startet und beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





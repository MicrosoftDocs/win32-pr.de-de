---
title: Ping
description: Verwenden Sie das pingpaket zum Herstellen einer Verbindung und Aushandeln der Sicherheit mit dem Server.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping-Bits
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "106340472"
---
# <a name="ping"></a>Ping

Verwenden Sie das **pingpaket** zum Herstellen einer Verbindung und Aushandeln der Sicherheit mit dem Server.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post
</dt> <dd>

Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.

Ersetzen Sie Remote-URL durch den absoluten oder relativen URI. Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp
</dt> <dd>

Identifiziert dieses Anforderungspaket als Ping-Paket.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **Ping** -Paket ist optional. Anstatt ein **Ping** -Paket zu senden, können Sie das Paket " [**Create-Session**](create-session.md) " verwenden, um eine Verbindung herzustellen und Sicherheit auszuhandeln. Es ist jedoch effizienter, das **Ping** -Paket zu diesem Zweck zu verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bestätigung für Ping**](ack-for-ping.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 





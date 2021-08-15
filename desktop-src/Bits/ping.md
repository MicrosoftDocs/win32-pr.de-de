---
title: Pingen
description: Verwenden Sie das Ping-Paket, um eine Verbindung herzustellen und die Sicherheit mit dem Server auszuhandeln.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping BITS
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479e03e6e18c0ec7421bd225744c5181029fc2b2e220f35c7bae7a3b02d42b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004890"
---
# <a name="ping"></a>Pingen

Verwenden Sie das **Ping-Paket,** um eine Verbindung herzustellen und die Sicherheit mit dem Server auszuhandeln.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

BITS-spezifisches Verb, das dieses Paket an den BITS-Server identifiziert.

Ersetzen Sie remote-URL durch den absoluten oder relativen URI. Ersetzen Sie remote-URL in der Regel durch den Remotedateinamen des Auftrags.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Anforderungspaket als Pingpaket.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **Pingpaket** ist optional. Anstatt ein **Pingpaket** zu senden, können Sie das [**Paket Create-Session**](create-session.md) verwenden, um eine Verbindung herzustellen und die Sicherheit auszuhandeln. Es ist jedoch effizienter, das **Ping-Paket** für diesen Zweck zu verwenden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ack für Ping**](ack-for-ping.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 





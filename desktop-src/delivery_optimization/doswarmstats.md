---
title: Doswarmstats-Struktur (deliveryoptimization. h)
description: Enthält Felder für das herunterladen und Hochladen von Statistiken für eine Datei.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Doswarmstats-Struktur
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346767"
---
# <a name="doswarmstats-structure"></a>Doswarmstats-Struktur

Enthält Felder für das herunterladen und Hochladen von Statistiken für eine Datei.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a>Member

<dl> <dt>

**fileId**
</dt> <dd>

Eine mit NULL endend beendete Zeichenfolge, die mit dem **ADDFILEWITHRANGES** -Befehl angegeben wurde.

</dd> <dt>

**SourceURL**
</dt> <dd>

NULL-terminierte Zeichenfolge, die den Namen der Datei auf dem Server enthält (z &lt; . b. https://Server &gt; / &lt; path &gt; /file.ext).

</dd> <dt>

**Filesize**
</dt> <dd>

Die Länge der Datei in Bytes.

</dd> <dt>

**totalbytesherunter geladen**
</dt> <dd>

Gesamtanzahl der übertragenen Bytes.

</dd> <dt>

**bytesfromlanpeers**
</dt> <dd>

Anzahl der von LAN-Peers übertragenen Bytes.

</dd> <dt>

**bytesfromgrouppeers**
</dt> <dd>

Anzahl von Bytes, die von Gruppen Peers übertragen werden.

</dd> <dt>

**bytesfrominternetpeers**
</dt> <dd>

Anzahl von Bytes, die von Internet Peers übertragen werden.

</dd> <dt>

**bytesfromhttp**
</dt> <dd>

Anzahl von Bytes, die von http übertragen werden.

</dd> <dt>

**bytesfromdoinc**
</dt> <dd>

Nur zur internen Verwendung.

</dd> <dt>

**bytestolanpeers**
</dt> <dd>

Anzahl der an LAN-Peers übertragenen Bytes.

</dd> <dt>

**bytestogrouppeers**
</dt> <dd>

Anzahl von Bytes, die an Gruppen Peers übertragen werden.

</dd> <dt>

**bytestointernetpeers**
</dt> <dd>

Anzahl von Bytes, die an Internet Peers übertragen werden.

</dd> <dt>

**httpconnectioncount**
</dt> <dd>

Anzahl der HTTP-Verbindungen.

</dd> <dt>

**doincconnectioncount**
</dt> <dd>

Nur zur internen Verwendung.

</dd> <dt>

**lanconnectioncount**
</dt> <dd>

Anzahl der LAN-Verbindungen.

</dd> <dt>

**groupconnectioncount**
</dt> <dd>

Anzahl der Gruppen Verbindungen.

</dd> <dt>

**internetconnectioncount**
</dt> <dd>

Anzahl der Internet Verbindungen.

</dd> <dt>

**Download Dauer**
</dt> <dd>

Dauer der Dateiübertragung in Millisekunden.

</dd> <dt>

**Download Mode**
</dt> <dd>

Der verwendete Download Modus finden Sie unter [**Download Mode**](downloadmode.md).

</dd> <dt>

**status**
</dt> <dd>

Zum Status einer Dateiübertragung finden Sie unter [**swarmstatus**](swarmstatus.md).

</dd> <dt>

**IsBackground**
</dt> <dd>

True, wenn es sich um eine Hintergrund Übertragung handelt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 






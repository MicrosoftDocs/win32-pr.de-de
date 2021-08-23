---
description: Weitere Informationen finden Sie unter Erweiterbare Storage Engine-Fehler.
title: Erweiterbare Storage Engine-Fehler
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0c0ee0a4423d5b37913bd7922af07a7b2196a30176b2a1adca37240e03a28594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721460"
---
# <a name="extensible-storage-engine-errors"></a>Erweiterbare Storage Engine-Fehler


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-errors"></a>Erweiterbare Storage Engine-Fehler

Alle möglichen Fehler, die von der ESE-API (Extensible Storage Engine) zurückgegeben werden, [werden](./jet-err.md) vom JET_ERR definiert. Eine Liste der Fehlerflags, die für diese API definiert sind, finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).

In der gesamten ESE-API-Dokumentation werden nur die wichtigsten Fehler dokumentiert. Diese Fehler stellen in der Regel API-Nutzungsfehler oder sehr wichtige Fehlerbedingungen dar. Beachten Sie, dass jede dieser ESE-APIs auch andere Fehler zurückgeben kann, die nicht für jede API dokumentiert sind. In diesen Fällen sollte der Aufrufer den Fehler wie jeder andere Fehler behandeln, der von der API zurückgegeben wird. Der spezifische Fehlerwert kann dann für Diagnosezwecke wie die Ablaufverfolgung verwendet werden.

Im Allgemeinen sollte ein Wert, der größer als 0 (null) ist, als Warnung interpretiert werden, der Wert 0 (null) sollte als Erfolg interpretiert werden, und ein Wert kleiner als 0 (null) sollte als Fehler interpretiert werden. Keine anderen Muster in diesen Werten (z. B. Wertebereiche) sollten von einer Anwendung verwendet werden.

Wenn ESE einige der schwerwiegenderen Fehler findet, wird ein Ereignisprotokolleintrag erstellt, der Details zu den Fehlern enthält. Die Protokollierungsebene kann durch [Ereignisprotokollparameter gesteuert werden.](./event-log-parameters.md)

Für einige Anwendungen ist es erforderlich, dass [JET_ERR](./jet-err.md)als HRESULTs zurückgeben können. Im folgenden C++-Beispiel wird die Konvertierung veranschaulicht:

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

Informationen zum Konfigurieren von Systemparametern für die Fehlerbehandlung finden Sie unter [Fehlerbehandlungsparameter](./error-handling-parameters.md).

### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)

[Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)

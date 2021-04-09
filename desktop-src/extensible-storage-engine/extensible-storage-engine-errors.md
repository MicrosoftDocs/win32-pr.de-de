---
description: Weitere Informationen finden Sie im Artikel zu Extensible Storage Engine-Fehlern.
title: Erweiterbare Speicher-Engine-Fehler
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868967"
---
# <a name="extensible-storage-engine-errors"></a>Erweiterbare Speicher-Engine-Fehler


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-errors"></a>Erweiterbare Speicher-Engine-Fehler

Alle möglichen Fehler, die von der ESE-API (Extensible Storage Engine) zurückgegeben werden, werden durch den [JET_ERR](./jet-err.md) -Datentyp definiert. Eine Liste der Fehlerflags, die für diese API definiert sind, finden Sie unter [Fehler Codes der Extensible Storage Engine](./extensible-storage-engine-error-codes.md).

In der gesamten ESE-API-Dokumentation werden nur die wichtigsten Fehler dokumentiert. Diese Fehlerstellen in der Regel API-Verwendungs Fehler oder sehr wichtige Fehlerbedingungen dar. Beachten Sie, dass jede dieser ESE-APIs auch andere Fehler zurückgeben kann, die für jede API nicht dokumentiert sind. In diesen Fällen sollte der Aufrufer einfach den Fehler behandeln, wie bei jedem anderen Fehler, der von der API zurückgegeben wird. Der spezifische Fehlerwert kann dann zu Diagnose Zwecken wie der Ablauf Verfolgung verwendet werden.

Im Allgemeinen sollte ein Wert, der größer als 0 (null) ist, als Warnung interpretiert werden. der Wert 0 (null) sollte als Success interpretiert werden, und ein Wert, der kleiner als 0 (null) ist, sollte als Fehler interpretiert werden. Keine anderen Muster in diesen Werten (z. b. Wertebereiche) sollten von einer Anwendung abhängig sein.

Wenn ESE auf einige der schwerwiegenderen Fehler stößt, wird ein Ereignisprotokoll Eintrag erstellt, der Details zu den Fehlern enthält. Die Protokollierungsebene kann durch [Ereignisprotokoll Parameter](./event-log-parameters.md)gesteuert werden.

Für einige Anwendungen ist es erforderlich, dass [JET_ERR](./jet-err.md)s als HRESULTs zurückgegeben werden. Im folgenden C++ Beispiel wird gezeigt, wie Sie diese Konvertierung vornehmen:

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

Weitere Informationen zum Konfigurieren von Systemparametern für die Fehlerbehandlung finden Sie unter Parameter für die [Fehlerbehandlung](./error-handling-parameters.md).

### <a name="see-also"></a>Weitere Informationen

[Fehler Behandlungsparameter](./error-handling-parameters.md)

[Fehler Codes für erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)

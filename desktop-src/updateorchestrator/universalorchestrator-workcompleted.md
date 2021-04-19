---
title: IUniversalOrchestrator::WorkCompleted
description: Ruft Universal Orchestrator auf, um anzugeben, dass die Arbeit fertig ist
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106369910"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>Iuniversalorchestrator:: workabgeschlossene-Methode

> [!NOTE] 
> Diese API gehört der universellen Orchestrator-API an.

Ermöglicht Clients, den universellen Orchestrator mitzuteilen, dass die zuvor geplante Arbeit abgeschlossen wurde, und beendet die Rückrufe, um die Arbeit bis zum nächsten erfolgreichen schedulework-Aufruf auszuführen.

## <a name="syntax"></a>Syntax

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Parameter

`callerIdentifier`

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.

`workCompleted`

**True** , wenn die Arbeit erfolgreich abgeschlossen wurde. Andernfalls **false** , wenn der arbeitsversuch fehlgeschlagen ist und in der Zukunft erneut versucht werden soll. 

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.  Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 




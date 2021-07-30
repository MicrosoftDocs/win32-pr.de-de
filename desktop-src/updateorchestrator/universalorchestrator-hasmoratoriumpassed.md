---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Fragt Universal Orchestrator ab, um zu ermitteln, ob der Zeitraum nach der OOBE überschritten wurde.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 3ccbf673b8fe22fabe7001112e04e87bd45eeaa4
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991797"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>IUniversalOrchestrator::HasFührungPassed-Methode

> [!NOTE] 
> Diese API gehört zur Universal Orchestrator-API.

Ermöglicht Clients, zu ermitteln, ob Universal Orchestrator unmittelbar nach dem neuen Out-of-Box-Gerät ausgeführt wird, wodurch Arbeitsversuche zur Minimierung von Benutzerunterbrechungen beschränkt werden. 

## <a name="syntax"></a>Syntax

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Parameter

`callerIdentifier`

Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.

`hasMoratoriumPassed`

Ausgabeparameter, der das Ergebnis der Abfrage speichert.

## <a name="return-value"></a>Rückgabewert
Wenn diese Methode erfolgreich ist, gibt **sie** S_OK.  Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Version |
|---|---|
| Unterstützte Mindestversion (Client) | Windows 10 1903 |
|   |   |



 

 




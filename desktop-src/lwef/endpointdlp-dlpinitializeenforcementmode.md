---
description: Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von DLP-Vorgängen (Endpoint Data Loss Prevention).
title: DlpInitializeEnforcementMode-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495730"
---
# <a name="dlpinitializeenforcementmode-function"></a>DlpInitializeEnforcementMode-Funktion

Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von Endpunktvorgängen zur Verhinderung von Datenverlust (Data Loss Prevention, DLP).

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Ein **DWORD,** das die Anzahl von Vorgängen angibt, die im *OperationEnforcement-Array* enthalten sind.

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[ In\]
</dt> <dd>

Ein Array von [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) Strukturen, die die Erzwingungsebene für einen Endpunkt-DLP-Vorgang angeben.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt ein HRESULT zurück, einschließlich, aber nicht beschränkt auf die folgenden Werte.

| HRESULT | BESCHREIBUNG |
|---------|-------------|
| S_OK | Die Funktion wurde erfolgreich abgeschlossen. |
| E_INVALIDARG | Mindestens einer der Funktionsparameter ist ungültig. |
| E_OUTOFMEMORY | Fehler bei der Speicherbelegung für den Vorgang. |



## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
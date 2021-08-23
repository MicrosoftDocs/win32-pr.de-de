---
description: Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von Endpunktvorgängen zur Verhinderung von Datenverlust (Data Loss Prevention, DLP).
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
ms.openlocfilehash: be1e71782b258745e31d286a69ae76d3ecbcafb74c170f3b5baf5eb19bcc4b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610440"
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

Ein **DWORD,** das die Anzahl der im *OperationEnforcement-Array enthaltenen Vorgänge an* gibt.

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[ In\]
</dt> <dd>

Ein Array von [DLP_APP_OP_ENLIGHTENED_LEVEL,](endpointdlp-dlp_app_op_enlightened_level.md) die die Erzwingungsebene für einen Endpunkt-DLP-Vorgang angeben.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt ein HRESULT zurück, einschließlich, aber nicht beschränkt auf die folgenden Werte.

| HRESULT | Beschreibung |
|---------|-------------|
| S_OK | Die Funktion wurde erfolgreich abgeschlossen. |
| E_INVALIDARG | Mindestens einer der Funktionsparameter ist ungültig. |
| E_OUTOFMEMORY | Fehler bei der Speicherzuweisung für den Vorgang. |



## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
---
description: Schätzt das Risiko der Ausführung von unbekanntem Code, wenn ein Handler für eine bestimmte Datei aufgerufen wird. Dieses Risiko basiert auf einem Verständnis des Handlers und des Codeinhalts der Datei.
title: EstimateFileRiskLevel-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841431"
---
# <a name="estimatefilerisklevel-function"></a>EstimateFileRiskLevel-Funktion

\[Diese Funktion ist unter Windows XP mit Service Pack 2 (SP2) über Windows Vista verfügbar. Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein. Clientanwendungen sollten stattdessen [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) verwenden, um eine Benutzerumgebung zu präsentieren, die einen sicheren Download und Austausch von Dateien über E-Mail- und Messaginganlagen ermöglicht.\]

Schätzt das Risiko der Ausführung von unbekanntem Code, wenn ein Handler für eine bestimmte Datei aufgerufen wird. Dieses Risiko basiert auf einem Verständnis des Handlers und des Codeinhalts der Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszFilePath* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad der Datei enthält, die für den Handler überprüft wird.

</dd> <dt>

*pszExt* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine mit NULL endende Zeichenfolge, die die Erweiterung der zu überprüfenden Datei enthält, entweder mit oder ohne führenden Punkt. Beispiel: ".txt" oder "txt".

</dd> <dt>

*pszHandler* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad des Handlers für die Datei enthält.

</dd> <dt>

*pfrlEstimate* \[ out\]
</dt> <dd>

Typ: **\_ \_ DATEIRISIKOSTUFE \***

Enthält nach erfolgreicher Rückgabe dieser Funktion einen Zeiger auf einen der folgenden Werte, der das geschätzte Risiko angibt.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ KEINE \_ MEINUNG** (0)


</dt> <dd>

Das Format der Datei wird nicht identifiziert, oder der Handler wird nicht identifiziert. Für eine aussagekräftige Antwort sind nicht genügend Informationen verfügbar.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)


</dt> <dd>

Das Format der Datei ist vollständig verständlich, der Handler ist bekannt, und es ist sehr sicher, dass kein überflüssiger Code ausgeführt wird.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERATE** (2)


</dt> <dd>

Das Format der Datei wird identifiziert, aber es ist nicht ausreichend verstanden, um als ein hohes oder niedriges Risiko zu bezeichnen.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ HIGH** (3)


</dt> <dd>

Das Dateiformat wird verstanden, und es wurden erhöhte Risikofaktoren identifiziert.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)


</dt> <dd>

Das Dateiformat wird speziell für diesen Handler blockiert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht in einem öffentlichen Header deklariert oder in einer Bibliotheksdatei enthalten. Um sie zu verwenden, müssen Sie sie direkt aus Winshfhc.dll von Ordnungszahl 101 laden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit \[ SP2-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (Version 5.1 oder höher)</dt> </dl> |



 

 





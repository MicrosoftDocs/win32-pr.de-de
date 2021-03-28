---
description: Schätzt das Risiko der Ausführung von unbekanntem Code, wenn ein Handler für eine bestimmte Datei aufgerufen wird. Dieses risikobasiert auf einem Verständnis des Handlers und des Code Inhalts der Datei.
title: Estimatefilerisklevel-Funktion
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
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980488"
---
# <a name="estimatefilerisklevel-function"></a>Estimatefilerisklevel-Funktion

\[Diese Funktion ist unter Windows XP mit Service Pack 2 (SP2) über Windows Vista verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar. Von Client Anwendungen sollte stattdessen [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) verwendet werden, um eine Benutzerumgebung bereitzustellen, die das sichere herunterladen und Austauschen von Dateien über e-Mail-und Messaging Anlagen ermöglicht.\]

Schätzt das Risiko der Ausführung von unbekanntem Code, wenn ein Handler für eine bestimmte Datei aufgerufen wird. Dieses risikobasiert auf einem Verständnis des Handlers und des Code Inhalts der Datei.

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

*pszfilepath* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Pfad der Datei enthält, die für den Handler überprüft wird.

</dd> <dt>

*pszext* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Erweiterung der zu überprüfenden Datei enthält, entweder mit oder ohne den führenden Zeitraum. Beispielsweise ". txt" oder "txt".

</dd> <dt>

*pszhandler* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Pfad des Handlers für die Datei enthält.

</dd> <dt>

*pfrlestimate* \[ vorgenommen\]
</dt> <dd>

Typ: **Datei \_ Risiko \_ Stufe \** _

Wenn diese Funktion erfolgreich zurückgegeben wird, enthält Sie einen Zeiger auf einen der folgenden Werte, die das geschätzte Risiko angeben.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ keine \_ Meinung** (0)


</dt> <dd>

Das Format der Datei wird nicht identifiziert, oder der Handler ist nicht identifiziert. Für eine sinnvolle Antwort sind nicht genügend Informationen verfügbar.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ Niedrig** (1)


</dt> <dd>

Das Format der Datei ist vollständig verständlich, der Handler ist bekannt, und es ist sehr sicher, dass kein überprüfbarer Code ausgeführt wird.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ Mittel (2** )


</dt> <dd>

Das Format der Datei wird zwar identifiziert, aber es ist nicht ausreichend verstanden, ob Sie als hohes oder niedriges Risiko gekennzeichnet werden soll.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ Hoch** (3)


</dt> <dd>

Das Dateiformat wird erkannt, und es wurden erhöhte Risikofaktoren erkannt.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ Block** (4)


</dt> <dd>

Das Dateiformat wird für diesen Handler speziell blockiert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einem öffentlichen Header deklariert oder in einer Bibliotheksdatei enthalten. Um es zu verwenden, müssen Sie es direkt aus Winshfhc.dll durch die Ordnungszahl 101 laden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (Version 5,1 oder höher)</dt> </dl> |



 

 





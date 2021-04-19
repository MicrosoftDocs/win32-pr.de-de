---
description: Ruft die Version der Endpunkt-DLP-API (Data Loss Prevention) auf dem aktuellen Gerät ab.
title: DlpGetEnforcementApiVersion-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495766"
---
# <a name="dlpgetenforcementapiversion-function"></a>DlpGetEnforcementApiVersion-Funktion

Ruft die Version der DLP-API (Data Loss Prevention) des Endpunkts auf dem aktuellen Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MajorVersion* \[ In\]
</dt> <dd>

Ein **DWORD,** das die Hauptversionsnummer angibt.

</dd> </dl>

<dl> <dt>

*MajorVersion* \[ In\]
</dt> <dd>

Ein **DWORD,** das die Nebenversionsnummer angibt.

</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt ein HRESULT zurück, einschließlich, aber nicht beschränkt auf die folgenden Werte.

| HRESULT | BESCHREIBUNG |
|---------|-------------|
| S_OK | Die Funktion wurde erfolgreich abgeschlossen. |




## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
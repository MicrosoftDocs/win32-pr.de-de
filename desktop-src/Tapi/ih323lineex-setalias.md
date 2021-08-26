---
description: Die SetAlias-Methode konfiguriert einen H.323-Standardalias für die Adresse. Dieser Alias wird im H.323-Aufrufsetupaustausch verwendet, damit die andere Partei den Namen dieser Partei kennt.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: IH323LineEx::SetAlias-Methode (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464c6707c3221fda1ef245e0302731ee7c6a1cf274c7ecac537c55f7f48437a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992190"
---
# <a name="ih323lineexsetalias-method"></a>IH323LineEx::SetAlias-Methode

\[**SetAlias** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetAlias-Methode** konfiguriert einen H.323-Standardalias für die Adresse. Dieser Alias wird im H.323-Aufrufsetupaustausch verwendet, damit die andere Partei den Namen dieser Partei kennt.

Wenn Sie diese Methode ein zweites Mal aufrufen, wird der vorherige Alias überschrieben.

Der für diese Schnittstelle festgelegte Alias wird nur verwendet, wenn es für den TSP keine andere Möglichkeit gibt, einen richtigen Alias zu finden. Wenn dem TSP in Zukunft Gatekeeper-Unterstützung hinzugefügt wird, überschreibt der alias, der beim Gatekeeper registriert oder vom Gatekeeper zugewiesen wird, alles, was über diese Methode festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strAlias* \[ In\]
</dt> <dd>

Der in Unicode zu verwendende Alias. **Die NULL-Terminierung** ist nicht erforderlich.

</dd> <dt>

*dwLength* \[ In\]
</dt> <dd>

Die Länge des Aliasnamens in Der  Anzahl von Zeichen, einschließlich des NULL-Abschlusszeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Methode war erfolgreich.<br/>                                                                                                     |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | Die anzahl der in *dwLength* angegebenen Zeichen überschreitet die tatsächliche Anzahl von Zeichen im *strAlias-Parameter.*<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 





---
description: Die put \_ FormatCodes-Methode legt die Liste der Formatcodes der Mediennutzlast fest. Die Variante enthält ein SAFEARRAY von BSTRs. Jeder BSTR innerhalb dieses Arrays ist eine Formatcodezeichenfolge.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: ITMedia::p ut_FormatCodes-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac8c2d9e102c6a923a535b8141c546885c583668e32fddb1fc607a8c1179a99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012960"
---
# <a name="itmediaput_formatcodes-method"></a>ITMedia::p ut \_ FormatCodes-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **put \_ FormatCodes-Methode** legt die Liste der Formatcodes der Mediennutzlast fest. Die Variante enthält ein SAFEARRAY von **BSTR** s. Jeder **BSTR** innerhalb dieses Arrays ist eine Formatcodezeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ In\]
</dt> <dd>

Liste der Mediennutzlastformatcodes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *NewVal-Parameter* ist ungültig.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Wenn eine Liste von Nutzlastformaten angegeben wird, bedeutet dies, dass alle diese Formate in der Sitzung verwendet werden können, aber das erste dieser Formate ist das Standardformat für die Sitzung. Wenn das Transportprotokoll RTP ist, sind die Formatcodes RTP-Nutzlasttypen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 





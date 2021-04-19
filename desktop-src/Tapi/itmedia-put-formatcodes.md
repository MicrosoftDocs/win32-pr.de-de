---
description: Mit der Put \_ Formatcodes-Methode wird die Liste der Formatcodes der Medien Nutzlast festgelegt. Die Variante enthält ein SafeArray von bstrinray. Jedes BSTR in diesem Array ist eine Format Code Zeichenfolge.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: ITmedia::p ut_FormatCodes-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352007"
---
# <a name="itmediaput_formatcodes-method"></a>ITmedia::p UT- \_ Formatcodes-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **Put \_ Formatcodes** -Methode wird die Liste der Formatcodes der Medien Nutzlast festgelegt. Die Variante enthält ein SafeArray von **BSTR** s. Jedes **BSTR** in diesem Array ist eine Format Code Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Die Liste der Formatcodes für Medien Nutzlast.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *NewVal* -Parameter ist ungültig.<br/>                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine Liste mit Nutz Last Formaten angegeben wird, bedeutet dies, dass alle diese Formate in der Sitzung verwendet werden können, aber das erste dieser Formate ist das Standardformat für die Sitzung. Wenn das Transportprotokoll RTP ist, sind die Formatcodes RTP-Nutz Last Typen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITmedia**](itmedia.md)
</dt> <dt>

[**ITmedia:: get- \_ Formatcodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 





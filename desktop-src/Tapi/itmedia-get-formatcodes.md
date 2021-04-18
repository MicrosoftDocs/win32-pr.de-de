---
description: Die get \_ Formatcodes-Methode ruft die Liste der Formatcodes der Medien Nutzlast ab. Die Variante gibt ein SafeArray von bstrinray zurück. Jedes BSTR in diesem Array ist eine Format Code Zeichenfolge.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'ITmedia:: get_FormatCodes-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352026"
---
# <a name="itmediaget_formatcodes-method"></a>ITmedia:: get \_ Formatcodes-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ Formatcodes** -Methode ruft die Liste der Formatcodes der Medien Nutzlast ab. Die Variante gibt ein SafeArray von **BSTR** s zurück. Jedes **BSTR** in diesem Array ist eine Format Code Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Array von Medien Nutzlast-Formatcodes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *PVal* -Parameter ist kein gültiger Zeiger.<br/>         |
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

[**ITmedia::p UT- \_ Formatcodes**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 





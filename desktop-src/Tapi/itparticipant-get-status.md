---
description: Die \_ Methode Get Status gibt einen Variant-booleschen Wert zurück, der den \_ Teilnehmer Status angibt
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Itteilnehmer:: get_Status-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357675"
---
# <a name="itparticipantget_status-method"></a>Itparticipants:: get \_ Status-Methode

\[**get \_ Der Status** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Methode **get \_ Status** gibt einen Variant-booleschen Wert zurück, der den \_ Teilnehmer Status angibt

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitstream* \[ in\]
</dt> <dd>

Zeiger auf die [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle.

</dd> <dt>

*pstatus* \[ vorgenommen\]
</dt> <dd>

Variant \_ true, wenn der Teilnehmer im Stream aktiviert ist, Variant \_ false, wenn er deaktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                              |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Die Methode ist nicht implementiert.<br/>                                        |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>           |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pitstream* -Parameter ist kein gültiger Zeiger.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pitstream* -Parameter verweist nicht auf eine gültige Schnittstelle.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Durch Aktivieren oder Deaktivieren des Status eines Teilnehmers für einen Stream kann eine Anwendung einen bestimmten Teilnehmer im wesentlichen stumm schalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> <dt>

[**Itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**Put- \_ Status**](itparticipant-put-status.md)
</dt> </dl>

 


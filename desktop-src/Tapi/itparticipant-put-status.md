---
description: Mit der Put \_ Status-Methode wird der Status eines Teilnehmers festgelegt.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: Itteilnehmer::p ut_Status-Methode (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368526"
---
# <a name="itparticipantput_status-method"></a>Itteilnehmer::p UT- \_ Status Methode

\[**Put \_ Der Status** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **Put \_ Status** -Methode wird der Status eines Teilnehmers festgelegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitstream* \[ in\]
</dt> <dd>

Zeiger auf die [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle.

</dd> <dt>

*fenckbar* \[ in\]
</dt> <dd>

Variant \_ true, wenn der Teilnehmer im Stream aktiviert ist, Variant \_ false, wenn er deaktiviert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                              |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Die Methode ist nicht implementiert.<br/>                                        |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pitstream* -Parameter ist kein gültiger Zeiger.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pitstream* -Parameter verweist nicht auf eine gültige Schnittstelle.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>           |



 

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

[**\_Status erhalten**](itparticipant-get-status.md)
</dt> </dl>

 


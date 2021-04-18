---
title: Iwmdrmnetreceiver processregistrationresponse-Methode (wmdrmsdk. h)
description: Die Methode processregistrationresponse verarbeitet eine vom Sender gesendete Registrierungs Antwort als Antwort auf eine Registrierungs Aufforderung.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Processregistrationresponse-Methode Windows Media-Format
- Processregistrationresponse-Methode Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, processregistrationresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358271"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>Iwmdrmnetreceiver::P rocess RegistrationResponse-Methode

Die Methode **processregistrationresponse** verarbeitet eine vom Sender gesendete Registrierungs Antwort als Antwort auf eine Registrierungs Aufforderung.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbregistrationresponse* \[ in\]
</dt> <dd>

Vom Sender empfangene Registrierungs Antwort.

</dd> <dt>

*cbregistrationresponse* \[ in\]
</dt> <dd>

Größe der Registrierungs Antwort in Bytes.

</dd> <dt>

*ppunkcancellationcookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert. Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird asynchron ausgeführt. Wenn die Verarbeitung abgeschlossen ist, wird das meproximitycomplete-Ereignis an die **imfmediaeventgenerator** -Schnittstelle gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnetreceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Iwmdrmnetreceiver:: getregistrationchallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 






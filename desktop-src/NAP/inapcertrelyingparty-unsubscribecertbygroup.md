---
title: INapCertRelyingParty UnSubscribeCertByGroup-Methode (NapCertRelyingParty.h)
description: Kündigen des Abonnements eines Integritätszertifikatservers (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- UnSubscribeCertByGroup-Methode NAP
- UnSubscribeCertByGroup-Methode NAP, INapCertRelyingParty-Schnittstelle
- INapCertRelyingParty-Schnittstelle NAP , UnSubscribeCertByGroup-Methode
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8b9f5398ba63c0e6108adfefd51d0546180db4536dbd95615e5b15dddde523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940218"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>INapCertRelyingParty::UnSubscribeCertByGroup-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **UnSubscribeCertByGroup-Methode** kündigen das Abonnement eines Integritätszertifikatservers (HCS).

## <a name="syntax"></a>Syntax


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *id* \[ in\]
</dt> <dd>

Eine [**EnforcementEntityId,**](nap-datatypes.md) die die ID des Nicht abonnierenden Erzwingungsclients enthält.

</dd> <dt>

 *reserviert* \[ In\]
</dt> <dd>

Muss **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn keine anderen HcS-Abonnenten vorhanden sind, löscht NapAgent die entsprechenden Integritätszertifikate aus dem lokalen Computerspeicher.

Rufen Sie vor dem Aufrufen dieser Methode [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapCertRelyingParty.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 






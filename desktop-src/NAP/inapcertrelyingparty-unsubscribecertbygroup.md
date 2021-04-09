---
title: Inapcertrelyingparty unabonniert bygroup-Methode (napcertrelyingparty. h)
description: Abonniert einen Integritäts Zertifikat Server (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Unabonniertbygroup-Methode NAP
- Unabonnebecertbygroup-Methode NAP, inapcertrelyingparty-Schnittstelle
- Inapcertrelyingparty Interface NAP, unabonnebecertbygroup-Methode
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
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956610"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>Inapcertrelyingparty:: unabonnebecertbygroup-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **unabonniertbygroup** -Methode entabonniert einen Integritäts Zertifikat Server (HCS).

## <a name="syntax"></a>Syntax


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *ID* \[ in\]
</dt> <dd>

Eine [**enforcemententityid**](nap-datatypes.md) , die die ID des Erzwingungs Clients enthält, der abonniert wird.

</dd> <dt>

 *reserviert* \[ in\]
</dt> <dd>

Muss **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn keine anderen Abonnenten für die HCS vorhanden sind, löscht der NAPAgent die entsprechenden Integritäts Zertifikate aus dem Speicher des lokalen Computers.

Rufen Sie vor dem Aufrufen dieser Methode " [**abonbecertbygroup**](inapcertrelyingparty-subscribecertbygroup.md)" auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Napcertrelyingparty. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcertrelyingparty. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapcertrelyingparty**](inapcertrelyingparty.md)
</dt> </dl>

 

 






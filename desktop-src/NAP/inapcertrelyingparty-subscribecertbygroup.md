---
title: Inapcertrelyingparty-Methode (abonniertbygroup) (napcertrelyingparty. h)
description: Abonniert einen Integritäts Zertifikat Server (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Abonniertbygroup-Methode, NAP
- Abonniertbygroup-Methode NAP, inapcertrelyingparty-Schnittstelle
- Inapcertrelyingparty-Schnittstelle NAP, abonniertbygroup-Methode
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339975"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>Inapcertrelyingparty:: abonbecertbygroup-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **abonniertbygroup** -Methode abonniert einen Integritäts Zertifikat Server (HCS). Die HCS müssen bereits registriert sein, bevor Sie abonniert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *ID* \[ in\]
</dt> <dd>

Eine [**enforcemententityid**](nap-datatypes.md) , die die ID des abonnierten Erzwingungs Clients enthält.

</dd> <dt>

*Abonnement Name* \[ in\]
</dt> <dd>

Der Name des Abonnenten.

> [!Note]  
> Dies wird zurzeit nur für Protokollierungs Zwecke verwendet.

 

</dd> <dt>

*reserviert* \[ in\]
</dt> <dd>

Muss **null** sein.

</dd> <dt>

*certexists* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob ein Integritäts Zertifikat von diesem HCS bereits vom NAPAgent verwaltet wird und im Computerspeicher vorhanden ist. **True** gibt an, dass ein Integritäts Zertifikat bereits verwaltet wird und vorhanden ist. Wenn der Wert **false** ist, wird ein Integritäts Zertifikat zurzeit nicht verwaltet und ist nicht vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

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

 

 






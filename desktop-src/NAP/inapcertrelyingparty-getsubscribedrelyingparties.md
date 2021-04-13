---
title: Inapcertrelyingparty getabonbedrelyingparties-Methode (napcertrelyingparty. h)
description: Ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Getabonbedrelyingparties-Methode NAP
- Getabonbedrelyingparties-Methode NAP, inapcertrelyingparty-Schnittstelle
- Inapcertrelyingparty-Schnittstelle NAP, getabonbedrelyingparties-Methode
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475489"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>Inapcertrelyingparty:: getabonbedrelyingparties-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getabonbedrelyingparties** -Methode ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**enforcemententitycount**](nap-datatypes.md) , die die Anzahl der abonnierten vertrauenden Seiten enthält.

</dd> <dt>

*relyingparties* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**enforcemententityid**](nap-datatypes.md) , die die Liste der abonnierten vertrauenden Seiten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss den Parameter *relyingparties* mithilfe von **CoTaskMemFree** freigeben.

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

 

 






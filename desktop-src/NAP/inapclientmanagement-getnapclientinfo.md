---
title: Inapclientmanagement getnapclientinfo-Methode (napmanagement. h)
description: Ruft Informationen zum NAP-Client ab.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Getnapclientinfo-Methode NAP
- Getnapclientinfo-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getnapclientinfo-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518245"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>Inapclientmanagement:: getnapclientinfo-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getnapclientinfo** -Methode ruft Informationen zum NAP-Client ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isnapabled* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen booleschen Wert, der auf **true** festgelegt ist, wenn NAP aktiviert ist. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

*Client Name* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die den Client Namen enthält.

</dd> <dt>

*clientdescription* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Client Beschreibung enthält.

</dd> <dt>

*ProtocolVersion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Protokollversion enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>       | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**RPC- \_ E \_ getrennt**</dt> </dl> | Der NAPAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Napmanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napmanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapclientmanagement**](inapclientmanagement.md)
</dt> </dl>

 

 






---
title: INapServerInfo GetNapServerInfo-Methode (NapServerManagement.h)
description: Ruft Informationen zum NAP-Server ab.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- NAP-Methode "GetNapServerInfo"
- GetNapServerInfo-Methode NAP, INapServerInfo-Schnittstelle
- INapServerInfo-Schnittstelle NAP, GetNapServerInfo-Methode
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eec9926e1a0bf94a1e3dac38c01a169d596c1c00bf032b8f6954f6331d5a4d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626130"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>INapServerInfo::GetNapServerInfo-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapServerInfo::GetNapServerInfo-Methode** ruft Informationen zum NAP-Server ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*serverName* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**CountedString-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) die den Servernamen enthält.

</dd> <dt>

*serverDescription* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**CountedString-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) die die Serverbeschreibung enthält.

</dd> <dt>

*protocolVersion* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**CountedString-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) die die Protokollversion enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 






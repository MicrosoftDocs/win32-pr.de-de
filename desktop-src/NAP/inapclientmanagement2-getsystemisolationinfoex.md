---
title: INapClientManagement2 getsystemisolationinfoex-Methode (napmanagement. h)
description: Ruft Informationen zum Isolations Status und zum erweiterten Isolations Status des napclient ab.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Getsystemisolationinfoex-Methode NAP
- Getsystemisolationinfoex-Methode NAP, INapClientManagement2-Schnittstelle
- INapClientManagement2 Interface NAP, getsystemisolationinfoex-Methode
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040406"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>INapClientManagement2:: getsystemisolationinfoex-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getsystemisolationinfoex** -Methode ruft Informationen über den Isolations Status und den erweiterten Isolations Status des napclient ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die Isolations Zustandsinformationen enthält.

</dd> <dt>

*unknownconnections* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen booleschen Wert, der **true** ist, wenn sich eine der Verbindungen in einem unbekannten Zustand befindet, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>       | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**RPC- \_ E \_ getrennt**</dt> </dl> | Der NAPAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Die abgerufenen Isolations Informationen spiegeln keine unbekannten Zustände wider.

Der SHA muss die [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur durch Aufrufen von [**freeisolationinfoex**](freeisolationinfoex.md)freigeben.

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

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 






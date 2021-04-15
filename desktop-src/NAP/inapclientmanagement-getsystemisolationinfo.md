---
title: Inapclientmanagement getsystemisolationinfo-Methode (napmanagement. h)
description: Ruft Informationen zum Isolations Status von napclient ab.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Getsystemisolationinfo-Methode NAP
- Getsystemisolationinfo-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getsystemisolationinfo-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392091"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>Inapclientmanagement:: getsystemisolationinfo-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getsystemisolationinfo** -Methode ruft Informationen zum Isolations Status von napclient ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die Isolations Zustandsinformationen enthält.

</dd> <dt>

*unknownconnections* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Flag, das angibt, ob sich eine der Verbindungen in einem unbekannten Zustand befindet. Wenn eine der beiden Werte ist, wird das-Flag auf **true** festgelegt. Andernfalls wird das-Flag auf **false** festgelegt.

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

 

 






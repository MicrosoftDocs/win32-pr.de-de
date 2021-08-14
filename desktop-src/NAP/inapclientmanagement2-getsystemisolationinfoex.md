---
title: INapClientManagement2 GetSystemIsolationInfoEx-Methode (NapManagement.h)
description: Ruft Informationen über den Isolationsstatus und den erweiterten Isolationsstatus von NapClient ab.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- GetSystemIsolationInfoEx-Methode NAP
- GetSystemIsolationInfoEx-Methode NAP, INapClientManagement2-Schnittstelle
- INapClientManagement2-Schnittstelle NAP, GetSystemIsolationInfoEx-Methode
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
ms.openlocfilehash: d03630cbd0647dc177460f92abc28e6aa66cbb663465ba7e9e93eefbc283ac00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621927"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>INapClientManagement2::GetSystemIsolationInfoEx-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **GetSystemIsolationInfoEx-Methode** ruft Informationen über den Isolationszustand und den erweiterten Isolationsstatus des NapClient ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfoEx-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) die Informationen zum Isolationszustand enthält.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Ein Zeiger auf eine BOOL, die **TRUE ist,** wenn sich eine der Verbindungen in einem unbekannten Zustand befindet, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl> | Der NapAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="remarks"></a>Hinweise

Die abgerufenen Isolationsinformationen spiegeln keine unbekannten Zustände wider.

Die SHA muss die [**IsolationInfoEx-Struktur durch**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) Aufrufen [**von FreeIsolationInfoEx frei geben.**](freeisolationinfoex.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 






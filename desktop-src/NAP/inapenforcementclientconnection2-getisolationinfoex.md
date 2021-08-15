---
title: INapEnforcementClientConnection2 GetIsolationInfoEx-Methode (NapEnforcementClient.h)
description: Wird verwendet, um Isolationsinformationen zum Client abzurufen.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- NAP-Methode "GetIsolationInfoEx"
- GetIsolationInfoEx-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2-Schnittstelle NAP , GetIsolationInfoEx-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89cc4a5fed046173ebdef2d5ed38574e52648fddd5cb357d8726c07581f51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368053"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a>INapEnforcementClientConnection2::GetIsolationInfoEx-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientConnection2::GetIsolationInfoEx-Methode** wird verwendet, um Isolationsinformationen zum Client abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfoEx-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) die die Konnektivitäts- und erweiterten Zustandsinformationen des Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Informationen werden von NapAgent nach der Verarbeitung einer [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festgelegt und dürfen nicht vom Erzwingungserzwinger festgelegt werden.

Der SHA muss die [**IsolationInfoEx-Struktur**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) durch Aufrufen von [**FreeIsolationInfoEx**](freeisolationinfoex.md)freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 






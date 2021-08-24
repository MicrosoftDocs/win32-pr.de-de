---
title: INapClientManagement RegisterSystemHealthAgent-Methode (NapManagement.h)
description: Registriert einen SHA beim NAP-System.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- RegisterSystemHealthAgent-Methode NAP
- RegisterSystemHealthAgent-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP , RegisterSystemHealthAgent-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e028e1f3dab17fb154ad1676acbf14fe1a31ce69a8f4c511e7f1447d2303bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803150"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>INapClientManagement::RegisterSystemHealthAgent-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **RegisterSystemHealthAgent-Methode** registriert einen SHA beim NAP-System.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Agent* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**NapComponentRegistrationInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die die Registrierungsinformationen für den SHA enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**IN \_ \_ KONFLIKTSTEHENDE \_ NAP E-ID**</dt> </dl> | Ein SHA, der diese ID verwendet, ist bereits registriert.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 






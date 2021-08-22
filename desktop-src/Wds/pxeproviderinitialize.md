---
title: PxeProviderInitialize-Rückruffunktion
description: Ein Export aus einer Anbieter-DLL (Dynamic Link Library), die den Anbieter initialisiert und für den Empfang von Clientanforderungen vorbereitet.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- PxeProviderInitialize-Rückruffunktion Windows Bereitstellungsdienste
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb7ba32049dc3ef70085a489b499d90b92ec6155323b650df0e2b2f839bbdf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098660"
---
# <a name="pxeproviderinitialize-callback-function"></a>PxeProviderInitialize-Rückruffunktion

Ein Export aus einer Anbieter-DLL (Dynamic Link Library), die den Anbieter initialisiert und für den Empfang von Clientanforderungen vorbereitet. Anbieter sind erforderlich, um die *PxeProviderInitialize-Funktion* zu exportieren. Alle Rückrufe an den Anbieter müssen während der Verarbeitung von *PxeProviderInitialize* mit einem Aufruf der [**PxeRegisterCallback-Funktion**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) registriert werden. Bei der Rückgabe dieser Funktion muss der Anbieter vollständig initialisiert und für die Verarbeitung von Clientanforderungen bereit sein.

## <a name="syntax"></a>Syntax


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProvider* \[ In\]
</dt> <dd>

Handle für die Anbieterinstanz. Dieses Handle muss vom Anbieter gespeichert und in allen nachfolgenden Aufrufen verwendet werden. Dieses Handle ist gültig, bis die [*Rückruffunktion PxeProviderShutdown*](pxeprovidershutdown.md) aufgerufen wird.

</dd> <dt>

*hProviderKey* \[ In\]
</dt> <dd>

Handle für einen Registrierungsschlüssel, in dem Anbieterkonfigurationsinformationen gespeichert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anbieterinitialisierung erfolgreich ist, sollte der Rückruf **ERROR \_ SUCCESS** zurückgeben. Im Falle eines Fehlers sollte ein geeigneter Fehlercode zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2003 mit \[ nur SP2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Serverfunktionen für Bereitstellungsdienste](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 






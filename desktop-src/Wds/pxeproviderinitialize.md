---
title: Pxeproviderinitialize-Rückruffunktion
description: Ein Export aus einer Anbieter-DLL (Dynamic Link Library), mit der der Anbieter initialisiert und für den Empfang von Client Anforderungen vorbereitet wird.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Pxeproviderinitialize-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342655"
---
# <a name="pxeproviderinitialize-callback-function"></a>Pxeproviderinitialize-Rückruffunktion

Ein Export aus einer Anbieter-DLL (Dynamic Link Library), mit der der Anbieter initialisiert und für den Empfang von Client Anforderungen vorbereitet wird. Anbieter müssen die *pxeproviderinitialize* -Funktion exportieren. Alle Rückrufe für den Anbieter müssen bei der Verarbeitung von *pxeproviderinitialize* mit einem Aufruf der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert werden. Bei der Rückgabe dieser Funktion muss der Anbieter vollständig initialisiert und bereit sein, Client Anforderungen zu verarbeiten.

## <a name="syntax"></a>Syntax


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprovider* \[ in\]
</dt> <dd>

Handle für die Anbieter Instanz. Dieses Handle muss vom Anbieter gespeichert und bei nachfolgenden Aufrufen verwendet werden. Dieses Handle ist gültig, bis die Rückruffunktion [*pxeprovidershutdown*](pxeprovidershutdown.md) aufgerufen wird.

</dd> <dt>

*hproviderkey* \[ in\]
</dt> <dd>

Handle für einen Registrierungsschlüssel, in dem Anbieter Konfigurationsinformationen gespeichert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anbieter Initialisierung erfolgreich ist, sollte der Rückruf einen **Fehler \_ Erfolg** zurückgeben. Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Server Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-server-functions.md)
</dt> <dt>

[*Pxeprovidershutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 






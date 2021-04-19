---
title: Pxeprovidershutdown-Rückruffunktion
description: Wird aufgerufen, um den Anbieter herunterzufahren.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Pxeprovidershutdown-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342428"
---
# <a name="pxeprovidershutdown-callback-function"></a>Pxeprovidershutdown-Rückruffunktion

Wird aufgerufen, um den Anbieter herunterzufahren. Diese Funktion wird durch Aufrufen der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert, wobei der *CallbackType* -Parameter auf den **PXE- \_ Rückruf \_ herunter** Gefahren festgelegt ist. Nachdem diese Funktion aufgerufen wurde, ist das an die [*pxeproviderinitialize*](pxeproviderinitialize.md) -Funktion weiter gegebene *hprovider* -Handle nicht mehr gültig.

## <a name="syntax"></a>Syntax


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ in\]
</dt> <dd>

Der Kontextwert, der an die [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion übergeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Anbieter erfolgreich heruntergefahren wurde, sollte der Rückruf einen **Fehler \_ Erfolg** zurückgeben. Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Server Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-server-functions.md)
</dt> <dt>

[*Pxeproviderinitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**Pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 






---
title: Pxeproviderservicecontrol-Rückruffunktion
description: Wird aufgerufen, wenn der WDS-Dienst einen Dienst Steuerungs Code empfängt.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Pxeproviderservicecontrol-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338147"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>Pxeproviderservicecontrol-Rückruffunktion

Wird aufgerufen, wenn der WDS-Dienst einen Dienst Steuerungs Code empfängt. Diese Rückruffunktion wird durch Aufrufen der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert, wobei der *CallbackType* -Parameter auf **PXE \_ Callback \_ Service \_ Control** festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ in\]
</dt> <dd>

Der Kontextwert, der an die [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion übergeben wird.

</dd> <dt>

*dwcontrol* 
</dt> <dd>

Steuerelement Code. Eine Liste der möglichen Werte finden Sie unter dem *dwcontrol* -Parameter der [*handlerex*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Funktion.

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

[**Pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 


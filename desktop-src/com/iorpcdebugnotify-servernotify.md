---
title: IOrpcDebugNotify-ServerNotify-Methode
description: Informiert den Server über eine eingehende Debuggeranforderung vom Client.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- ServerNotify-Methode COM
- Com-Methode "ServerNotify", IOrpcDebugNotify-Schnittstelle
- IOrpcDebugNotify-Schnittstelle COM, ServerNotify-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff0faac4ee4e5fa691088afa9de8871a8bf9382ce3da629b3fc14dd9d932ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048098"
---
# <a name="iorpcdebugnotifyservernotify-method"></a>IOrpcDebugNotify::ServerNotify-Methode

Informiert den Server über eine eingehende Debuggeranforderung vom Client.

> [!Note]  
> Eine Importbibliothek, die die **ServerNotify-Funktion** enthält, ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die [**Funktionen GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um einen Funktionszeiger auf [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) aus oleaut.dll abzurufen und diese Funktion über die [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) zur Verfügung zu stellen.

 

## <a name="syntax"></a>Syntax


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ DBG \_ ALL-Struktur,**](orpc-dbg-all.md) die benachrichtigungsspezifische Informationen enthält, die das COM RPC-System an den Debugger übergibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 


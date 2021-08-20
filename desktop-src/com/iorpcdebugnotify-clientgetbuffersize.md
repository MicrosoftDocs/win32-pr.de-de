---
title: IOrpcDebugNotify ClientGetBufferSize-Methode
description: Ruft die RPC-Puffergröße vom clientseitigen Debugger ab.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- ClientGetBufferSize-Methode COM
- ClientGetBufferSize-Methode COM, IOrpcDebugNotify-Schnittstelle
- IOrpcDebugNotify-Schnittstelle COM, ClientGetBufferSize-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038273dfd93264d483bacb314b78e33f3e8f16cef4f120be27bd48901ef5b060
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859470"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a>IOrpcDebugNotify::ClientGetBufferSize-Methode

Ruft die RPC-Puffergröße vom clientseitigen Debugger ab.

> [!Note]  
> Eine Importbibliothek, die die **ClientGetBufferSize-Funktion** enthält, ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um einen Funktionszeiger auf [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) aus oleaut.dll abzurufen und diese Funktion über die [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) bereitzustellen.

 

## <a name="syntax"></a>Syntax


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ DBG \_ ALL-Struktur,**](orpc-dbg-all.md) die Benachrichtigungsinformationen enthält, die das COM-RPC-System an den Debugger übergibt.

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

 


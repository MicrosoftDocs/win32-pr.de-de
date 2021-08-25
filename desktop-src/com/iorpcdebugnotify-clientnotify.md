---
title: IOrpcDebugNotify-ClientNotify-Methode
description: Informiert den Client über eine ausgehende Debuggeranforderung an den Server.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- ClientNotify-Methode COM
- ClientNotify-Methode COM, IOrpcDebugNotify-Schnittstelle
- IOrpcDebugNotify-Schnittstelle COM, ClientNotify-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc80262b75bb170f14fa191f5a60e658cd371765714860f09a7bbcadcbcc369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854280"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a>IOrpcDebugNotify::ClientNotify-Methode

Informiert den Client über eine ausgehende Debuggeranforderung an den Server.

> [!Note]  
> Eine Importbibliothek, die **die ClientNotify-Funktion** enthält, ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die [**Funktionen GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um einen Funktionszeiger auf [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) aus oleaut.dll abzurufen und diese Funktion über die [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) zur Verfügung zu stellen.

 

## <a name="syntax"></a>Syntax


```C++
void ClientNotify(
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

## <a name="requirements"></a>Requirements (Anforderungen)



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

 


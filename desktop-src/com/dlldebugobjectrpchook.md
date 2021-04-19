---
title: Dlldebugobjectrpchook-Funktion
description: Exportiert durch COM-DLLs zum Aktivieren des Remote Debuggens.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- Dlldebugobjectrpchook-Funktion com
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345932"
---
# <a name="dlldebugobjectrpchook-function"></a>Dlldebugobjectrpchook-Funktion

Exportiert durch COM-DLLs zum Aktivieren des Remote Debuggens.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ablaufverfolgungs-* 
</dt> <dd>

**True** gibt an, dass Remote Debugging aktiviert ist. **False** gibt an, dass Remote Debugging nicht aktiviert ist.

</dd> <dt>

*lporpcinitargs* 
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ Init \_ args**](orpc-init-args.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORPC \_ dbg \_ alle**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ dbg- \_ Puffer**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC-init-Argumente \_ \_**](orpc-init-args.md)
</dt> <dt>

[**Iorpcdebug-Benachrichtigung**](iorpcdebugnotify.md)
</dt> </dl>

 

 






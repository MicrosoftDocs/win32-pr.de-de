---
title: Tfguidatom (msctf. h)
description: Der tfguidatom-Datentyp identifiziert eine GUID in TSF. Ein tfguidatom wird durch Aufrufen von itfcategorymgr registerguid abgerufen.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- Tfguidatom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102827"
---
# <a name="tfguidatom"></a>Tfguidatom

Der **tfguidatom** -Datentyp identifiziert eine **GUID** in TSF. Ein **tfguidatom** wird durch Aufrufen von [**itfcategorymgr:: registerguid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)abgerufen.


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a>Bemerkungen

Ein **tfguidatom** -Wert ist nur innerhalb des Prozesses gültig, von dem **itfcategorymgr:: registerguid** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITF categorymgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[**ITF categorymgr:: isequaltf guidatom**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[**ITF categorymgr:: registerguid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 






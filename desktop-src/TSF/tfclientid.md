---
title: Tfclientid (msctf. h)
description: Der tfclientid-Datentyp wird verwendet, um den Client zu identifizieren.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- Tfclientid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740873"
---
# <a name="tfclientid"></a>Tfclientid

Der **tfclientid-** Datentyp wird verwendet, um den Client zu identifizieren.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Bemerkungen

In TSF werden Anwendungen und Text Dienste im Allgemeinen als Clients bezeichnet. Jeder Client erhält einen eindeutigen Bezeichner, den er verwendet, um sich selbst zu identifizieren, wenn verschiedene TSF Manager-Methoden aufgerufen werden. Dieser Bezeichner weist den **tfclientid-** Typ auf.

Der **tfclientid-** Datentyp wird vom TSF-Manager bereitgestellt. Eine Anwendung erhält einen **tfclientid-** Wert, wenn [ITfThreadMgr:: Aktivierung](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)aufgerufen wird. Der tfclientid-Wert für einen Text Dienst wird an die [itftextinputprocessor:: Aktivierungs](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) -Methode übergeben. Alle Objekte, die nicht in die obigen Kategorien passen, können durch Aufrufen von [itfclientid:: getClientID](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)einen Client Bezeichner abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                          |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITF ClientID:: getClientID**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITF textinputprocessor:: Aktivierung**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr:: Aktivieren**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 






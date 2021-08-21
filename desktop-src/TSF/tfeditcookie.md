---
title: TfEditCookie (Msctf.h)
description: Der TfEditCookie-Datentyp identifiziert eine Bearbeitungssitzung mit einer Sperre.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa397354ea7aa8addca4008d321162a99073345efc0761b65687f704a573ef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874078"
---
# <a name="tfeditcookie"></a>TfEditCookie

Der **TfEditCookie-Datentyp** identifiziert eine Bearbeitungssitzung mit einer Sperre.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Hinweise

Der **TfEditCookie-Datentyp** wird vom TSF-Manager bereitgestellt und von einem Client (Anwendung oder Textdienst) verwendet, um eine Bearbeitungssitzung mit einer schreibgeschützten oder Lese-/Schreibsperre in verschiedenen Methoden zu identifizieren.

Ein **TfEditCookie-Wert** wird auf eine der folgenden Arten erhalten.

-   Der Client ruft [ITfDocumentMgr::CreateContext auf.](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
-   Der TSF-Manager ruft die [ITfEditSession::D oEditSession-Methode des Clients](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) auf.
-   Der TSF-Manager ruft die [ITfCompositionSink::OnCompositionTerminated-Clientmethode](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) auf.
-   Der TSF-Manager ruft die [ITfCleanupContextSink::OnCleanupContext-Clientmethode](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) auf.
-   Der TSF-Manager ruft die [ITfTextEditSink::OnEndEdit-Clientmethode](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITfCleanupContextSink::OnCleanupContext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITfCompositionSink::OnCompositionTerminated**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr::CreateContext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**ITfEditSession::D oEditSession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITfTextEditSink::OnEndEdit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 






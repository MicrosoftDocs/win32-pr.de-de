---
title: Tfeditcookie (msctf. h)
description: Der tfeditcookie-Datentyp identifiziert eine Bearbeitungs Sitzung, die über eine Sperre verfügt.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- Tfeditcookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040060"
---
# <a name="tfeditcookie"></a>Tfeditcookie

Der **tfeditcookie** -Datentyp identifiziert eine Bearbeitungs Sitzung, die über eine Sperre verfügt.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Bemerkungen

Der **tfeditcookie** -Datentyp wird vom TSF-Manager bereitgestellt und wird von einem Client (Anwendungs-oder Text Dienst) verwendet, um eine Bearbeitungs Sitzung mit einer Lese-oder Lese-/Schreibsperre in verschiedenen Methoden zu identifizieren.

Ein **tfeditcookie** -Wert wird auf eine der folgenden Arten abgerufen.

-   Der Client ruft [ITF documentmgr:: featecontext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)auf.
-   Der TSF-Manager ruft die Client- [itfedizession::D oedizession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) -Methode auf.
-   Der TSF-Manager ruft die [ITF compositionsink:: oncompositionbeendete](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) -Methode des Clients auf.
-   Der TSF-Manager ruft die [ITF cleanupcontextsink:: oncleanupcontext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) -Methode des Clients auf.
-   Der TSF-Manager ruft die [itbtexteditsink:: onendedit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) -Client Methode auf.

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

[**ITF cleanupcontextsink:: oncleanupcontext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITF compositionsink:: oncompositionbeendete**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITF documentmgr:: kreatecontext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**Itfedizession::D oedizession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITF texteditsink:: onendedit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 






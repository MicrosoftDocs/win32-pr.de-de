---
description: Fordert an, dass der System Treiber Dienst seinen Status auf Service Manager aktualisiert.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: InterrogateService-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126481"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a>InterrogateService-Methode der Win32 \_ systemdriver-Klasse

Die Methode " **InterrogateService** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " fordert an, dass der System Treiber Dienst seinen Status auf den Dienst-Manager aktualisiert.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert von 0 (null) zurück, wenn die Anfrage **gateservice** -Anforderung akzeptiert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ System Treiber**](win32-systemdriver.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ baseservice**](win32-baseservice.md)
</dt> </dl>

 


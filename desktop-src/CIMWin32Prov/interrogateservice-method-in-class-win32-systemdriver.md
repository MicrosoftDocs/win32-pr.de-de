---
description: Fordert an, dass der Systemtreiberdienst seinen Zustand auf den Dienst-Manager aktualisiert.
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
ms.openlocfilehash: 0327dc7dcb357217ff18df85b22c7cc7bff8972f42ebeb53a89f552c98205d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760330"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a>InterrogateService-Methode der Win32 \_ SystemDriver-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** fordert an, dass der Systemtreiberdienst seinen Zustand auf den Dienst-Manager aktualisiert.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die **InterrogateService-Anforderung** akzeptiert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 


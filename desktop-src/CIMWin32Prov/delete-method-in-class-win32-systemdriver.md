---
description: 'Delete-Methode der Win32_SystemDriver-Klasse: Delete&\# 8194; Die WMI-Klassenmethode löscht einen vorhandenen Dienst.'
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Delete-Methode der Win32_SystemDriver Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097088"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a>Delete-Methode der Win32 \_ SystemDriver-Klasse

Die **Delete** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht einen vorhandenen Dienst.

In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich gelöscht wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 


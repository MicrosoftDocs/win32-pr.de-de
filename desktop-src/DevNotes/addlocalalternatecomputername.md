---
description: Fügt für den Computer, von dem Sie aufgerufen wird, einen alternativen lokalen Netzwerknamen hinzu.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Addlocalalternativen Computername-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361628"
---
# <a name="addlocalalternatecomputername-function"></a>Addlocalalternativen Computername-Funktion

Fügt für den Computer, von dem Sie aufgerufen wird, einen alternativen lokalen Netzwerknamen hinzu.

## <a name="syntax"></a>Syntax


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpdnsfqhostname* \[ in\]
</dt> <dd>

Der Alternative Name, der hinzugefügt werden soll. Der Name muss das Format " **computernamednsfullyqualified** " aufweisen, wie in der-Enumeration des [**Computer \_ Namen \_ Formats**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) definiert, und die [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) -Funktion muss Sie in der Lage sein, Sie zu validieren, wenn ihr Format auf **dnsnamehostnamefull** festgelegt ist.

</dd> <dt>

*ulflags* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion den **Fehler \_ Erfolg** zurück. Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich 0 (null) zurückgegeben. Zu den zurückgegebenen Fehlercodes zählen die folgenden:



| Rückgabecode                                                                                               | Beschreibung                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>  | Gibt an, dass der *lpdnsfqhostname* -Parameter nicht auf einen gültigen DNS-Namen verweist oder dass der *ulflags* -Parameter ungleich 0 (null) ist.<br/> |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl> | Es steht nicht genügend Arbeitsspeicher zur Verfügung, um den Vorgang durchzuführen.<br/>                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Bibliothek<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Unicode- und ANSI-Name<br/> | **Addlocalalternativen computernamew** (Unicode) und **addlocalalternativen computernamea** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Format des Computer \_ namens \_**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 

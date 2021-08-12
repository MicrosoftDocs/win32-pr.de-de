---
description: Fügt einen alternativen lokalen Netzwerknamen für den Computer hinzu, von dem aus er aufgerufen wird.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName-Funktion
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
ms.openlocfilehash: 90945188209abdcaf16a7250e43db2af9a99ab4a3fbb55b8baabf0ea610c99e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668682"
---
# <a name="addlocalalternatecomputername-function"></a>AddLocalAlternateComputerName-Funktion

Fügt einen alternativen lokalen Netzwerknamen für den Computer hinzu, von dem aus er aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpDnsFQHostname* \[ In\]
</dt> <dd>

Der alternative Name, der hinzugefügt werden soll. Der Name muss im **ComputerNameDnsFullyQualified-Format** vorliegen, wie in der [**COMPUTER NAME \_ \_ FORMAT-Enumeration**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) definiert, und die [**W-Funktion DnsValidateName \_**](/windows/win32/api/windns/nf-windns-dnsvalidatename) muss in der Lage sein, ihn mit dem Format **dnsNameHostnameFull** zu überprüfen.

</dd> <dt>

*ulFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion **ERROR \_ SUCCESS zurück.** Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich 0 (null) zurückgegeben. Zu den zurückgegebenen Fehlercodes gehören die folgenden:



| Rückgabecode                                                                                               | Beschreibung                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>  | Gibt an, dass der *lpDnsFQHostname-Parameter* nicht auf einen gültigen DNS-Namen verweist oder dass der *ulFlags-Parameter* ungleich 0 (null) ist.<br/> |
| <dl> <dt>**FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl> | Es steht nicht genügend Arbeitsspeicher zur Verfügung, um den Vorgang durchzuführen.<br/>                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Bibliothek<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Unicode- und ANSI-Name<br/> | **AddLocalAlternateComputerNameW** (Unicode) und **AddLocalAlternateComputerNameA** (ANSI)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_FORMAT DES \_ COMPUTERNAMENS**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 

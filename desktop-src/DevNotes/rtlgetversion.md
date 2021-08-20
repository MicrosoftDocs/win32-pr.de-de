---
description: Ruft Versionsinformationen zum derzeit ausgeführten Betriebssystem ab.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: RtlGetVersion-Funktion (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: 7420b9dba03e3b136331f4463f476908882ca5564d0fc7ac563036c7acccb356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161682"
---
# <a name="rtlgetversion-function"></a>RtlGetVersion-Funktion

Ruft Versionsinformationen zum derzeit ausgeführten Betriebssystem ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpVersionInformation* \[ out\]
</dt> <dd>

Zeiger auf eine [**RTL \_ OSVERSIONINFOW-Struktur**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) oder eine [**RTL \_ OSVERSIONINFOEXW-Struktur,**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) die die Versionsinformationen zum derzeit ausgeführten Betriebssystem enthält. Ein Aufrufer gibt an, welche Eingabestruktur verwendet wird, indem der **dwOSVersionInfoSize-Member** der -Struktur auf die Größe der verwendeten Struktur in Bytes festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt STATUS \_ SUCCESS zurück.

## <a name="remarks"></a>Hinweise

**RtlGetVersion** entspricht der [**GetVersionEx-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) im Windows SDK. Sehen Sie sich das Beispiel im Windows SDK an, das zeigt, wie Sie die Systemversion erhalten.

Bei Verwendung **von RtlGetVersion,** um zu bestimmen, ob eine bestimmte Version des Betriebssystems ausgeführt wird, sollte ein Aufrufer nach Versionsnummern suchen, die größer oder gleich der erforderlichen Versionsnummer sind. Dadurch wird sichergestellt, dass ein Versionstest für spätere Versionen von Windows.

Da Betriebssystemfeatures in einer verteilbaren DLL hinzugefügt werden können, ist die Überprüfung nur der Haupt- und Nebenversionsnummern nicht die zuverlässigste Möglichkeit, das Vorhandensein eines bestimmten Systemfeatures zu überprüfen. Ein Treiber sollte [**RtlVerifyVersionInfo verwenden,**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) um das Vorhandensein eines bestimmten Systemfeatures zu testen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Header<br/>                   | <dl> <dt>Ntddk.h (einschließlich Ntddk.h)</dt> </dl>                                                     |
| Bibliothek<br/>                  | <dl> <dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 

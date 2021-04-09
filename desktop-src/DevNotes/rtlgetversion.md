---
description: Ruft Versionsinformationen zum aktuell laufenden Betriebssystem ab.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Rtlgetversion-Funktion (ntddk. h)
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
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126404"
---
# <a name="rtlgetversion-function"></a>Rtlgetversion-Funktion

Ruft Versionsinformationen zum aktuell laufenden Betriebssystem ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpversioninformation* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [**RTL \_ osversioninfow**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) -Struktur oder eine [**RTL \_ osversioninfoexw**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) -Struktur, die die Versionsinformationen zum aktuell ausgelaufenden Betriebssystem enthält. Ein Aufrufer gibt an, welche Eingabe Struktur verwendet wird, indem der **dwOSVersionInfoSize** -Member der-Struktur auf die Größe in Bytes der verwendeten Struktur festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Status \_ Erfolg zurück.

## <a name="remarks"></a>Bemerkungen

**Rtlgetversion** ist die Entsprechung der [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) -Funktion in der Windows SDK. Sehen Sie sich das Beispiel in der Windows SDK an, in dem gezeigt wird, wie Sie die System Version erhalten.

Wenn Sie **rtlgetversion** verwenden, um zu bestimmen, ob eine bestimmte Version des Betriebssystems ausgeführt wird, muss ein Aufrufer nach Versionsnummern suchen, die größer oder gleich der erforderlichen Versionsnummer sind. Dadurch wird sichergestellt, dass ein Versions Test für spätere Versionen von Windows erfolgreich ist.

Da Betriebssystemfunktionen in einer verteilbaren dll hinzugefügt werden können, ist die Überprüfung nur der Haupt-und neben Versionsnummern nicht die zuverlässigste Möglichkeit, das vorhanden sein eines bestimmten System Features zu überprüfen. Ein Treiber sollte [**rtlverifyversioninfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) verwenden, um zu testen, ob eine bestimmte Systemfunktion vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Header<br/>                   | <dl> <dt>Ntddk. h (einschließlich ntddk. h)</dt> </dl>                                                     |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib; </dt> <dt>Nzu-nl. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Psgetversion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 

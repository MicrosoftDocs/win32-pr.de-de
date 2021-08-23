---
description: Lädt die angegebene Registrierungsstrukturdatei in den Arbeitsspeicher und überprüft die Struktur.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: OROpenHive-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 86ff3d6ff15b030054d40ca7131e521cedb59ebf20c4942951f0e141f27a2840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076014"
---
# <a name="oropenhive-function"></a>OROpenHive-Funktion

Lädt die angegebene Registrierungsstrukturdatei in den Arbeitsspeicher und überprüft die Struktur.

## <a name="syntax"></a>Syntax


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpHivePath* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen der Registrierungsstrukturdatei angibt, die in den Arbeitsspeicher geladen werden soll. Dies kann eine Hive-Datei sein, die mit der [**ORSaveHive-Funktion**](orsavehive.md) gespeichert oder mit der [RegSaveKey-](/windows/win32/api/winreg/nf-winreg-regsavekeya) oder [RegSaveKeyEx-Funktion](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) erstellt wurde. Die Datei muss weniger als 4 GB groß sein, und der Aufrufer muss \_ über FILE READ \_ DATA-Zugriff auf die Datei verfügen. Weitere Informationen finden Sie unter [Dateisicherheit und Zugriffsrechte.](../fileio/file-security-and-access-rights.md)

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den Stammschlüssel der geladenen Offlineregistrierungsstruktur empfängt. Wenn die Registrierungsstrukturdatei nicht geöffnet werden kann oder die Überprüfung fehlschlägt, legt die Funktion diesen Parameter auf **NULL** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen. Mögliche Fehlercodes sind:

-   Wenn die Datei leer oder größer als 4 GB ist, gibt die Funktion ERROR \_ BADDB zurück.
-   Wenn der Aufrufer nicht über die erforderlichen Zugriffsrechte zum Öffnen der Datei verfügt, gibt die Funktion ERROR \_ ACCESS \_ DENIED zurück.
-   Wenn die Überprüfung der Registrierungsstruktur fehlschlägt, gibt die Funktion ERROR \_ NOT \_ REGISTRY FILE \_ zurück.

## <a name="remarks"></a>Hinweise

Die **OROpenHive-Funktion** ist die einzige Offlineregistrierungsfunktion, die eine Registrierungsstruktur überprüft. Wenn die Überprüfung fehlschlägt, wird nicht versucht, die Struktur zu reparieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 

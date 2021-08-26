---
description: Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: ORDeleteValue-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 717464b1ba44593a9b36ccf26e5df248cb95df9bfa40a7786896c87041e246d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045290"
---
# <a name="ordeletevalue-function"></a>ORDeleteValue-Funktion

Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

## <a name="syntax"></a>Syntax


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*lpValueName* \[ in, optional\]
</dt> <dd>

Der zu entfernende Registrierungswert. Wenn dieser Parameter **NULL oder** eine leere Zeichenfolge ist, wird der von der [**ORSetValue-Funktion**](orsetvalue.md) festgelegte unbenannte Standardwert entfernt.

Bei Wertnamen wird die Schreibung nicht beachtet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerfreier Code, der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem Flag FORMAT \_ MESSAGE FROM SYSTEM \_ \_ verwenden, um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offlineregistrierungsbibliothek, Version 1.0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 

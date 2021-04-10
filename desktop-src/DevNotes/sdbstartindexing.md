---
description: Ermöglicht das Erstellen und Ändern von Indizes für die angegebene Datenbank.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: Sdbstartindex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126391"
---
# <a name="sdbstartindexing-function"></a>Sdbstartindex-Funktion

Ermöglicht das Erstellen und Ändern von Indizes für die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*iiwhat* \[ in\]
</dt> <dd>

Der Indexbezeichner

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbcommitindexes**](sdbcommitindexes.md)
</dt> <dt>

[**Sdbdeclareingedex**](sdbdeclareindex.md)
</dt> <dt>

[**Sdbstopindizierung**](sdbstopindexing.md)
</dt> </dl>

 

 





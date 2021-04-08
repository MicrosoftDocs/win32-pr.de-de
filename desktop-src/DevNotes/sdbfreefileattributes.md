---
description: Gibt die angegebenen Datei Attributdaten frei.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Sdbfrefileattribute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747688"
---
# <a name="sdbfreefileattributes-function"></a>Sdbfrefileattribute-Funktion

Gibt die angegebenen Datei Attributdaten frei.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfileattribute* \[ in\]
</dt> <dd>

Eine [**attrinfo**](attrinfo.md) -Struktur, die von der [**sdbgetfileattribute**](sdbgetfileattributes.md) -Funktion zurückgegeben wird.

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

[**Sdbgetfileattribute**](sdbgetfileattributes.md)
</dt> </dl>

 

 





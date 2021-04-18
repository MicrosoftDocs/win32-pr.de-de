---
title: Frefixupinfo-Funktion (naputil. h)
description: Gibt eine fixupinfo-Datenstruktur frei.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Funktion "frefixupinfo" NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343869"
---
# <a name="freefixupinfo-function"></a>Frefixupinfo-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die Funktion " **frefixupinfo** " gibt eine [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Datenstruktur frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fixupinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die Datenstruktur " [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) ", die freigegeben werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):

-   **In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.
-   Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.
-   **In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.

Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Naputil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zuordnung von "Zuweisung"**](allocfixupinfo-func.md)
</dt> </dl>

 

 






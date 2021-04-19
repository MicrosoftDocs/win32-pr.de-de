---
title: Freeisolationinfo-Funktion (naputil. h)
description: Gibt eine IsolationInfo-Datenstruktur frei.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- Freeisolationinfo-Funktion NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345320"
---
# <a name="freeisolationinfo-function"></a>Freeisolationinfo-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **freeisolationinfo** -Funktion gibt eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Datenstruktur frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die zu freie [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Datenstruktur.

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



 

 






---
title: Freeisolationinfoex-Funktion (naputil. h)
description: Gibt eine isolationinfoex-Datenstruktur frei.
ms.assetid: 9ca0e5ae-aed9-43e9-b8f7-90f13d62ac16
keywords:
- Freeisolationinfoex-Funktion NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfoEx
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cf3f13f38130fe86383fee5bebe3a536ea9aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105422"
---
# <a name="freeisolationinfoex-function"></a>Freeisolationinfoex-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **freeisolationinfoex** -Funktion gibt eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Datenstruktur frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeIsolationInfoEx(
  _In_ IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die frei verfügbaren [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Datenstruktur.

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



 

 






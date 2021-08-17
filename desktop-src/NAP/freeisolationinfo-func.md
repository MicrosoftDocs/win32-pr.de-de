---
title: FreeIsolationInfo-Funktion (NapUtil.h)
description: Gibt eine IsolationInfo-Datenstruktur frei.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- NAP-Funktion "FreeIsolationInfo"
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
ms.openlocfilehash: 031fd49bbdda7c0b36481776ba3c9dca8ea6d1c236b0010ada319b9a51f989df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940647"
---
# <a name="freeisolationinfo-function"></a>FreeIsolationInfo-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **FreeIsolationInfo-Funktion** gibt eine [**IsolationInfo-Datenstruktur**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ In\]
</dt> <dd>

Ein Zeiger [](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) auf die isolationInfo-Datenstruktur, die freigegeben werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle com-Schnittstellen, die vom NAP-System unterstützt werden, verwenden COM-Standardspeicherverwaltungsregeln und die COM-Speicherbezuweisungen (**CoTaskMemAlloc** und **CoTaskMemFree**):

-   **In** werden Parameter vom Aufrufer zugeordnet und freigegeben.
-   **Out-Parameter** werden vom Aufgerufenen zugeordnet und vom Aufrufer mit **coTaskMem** freigegeben.
-   **Ein-/Aus-Parameter** werden vom Aufrufer zugeordnet, vom Aufgerufenen freigegeben und neu zugeordnet und schließlich vom Aufrufer freigegeben, indem **CoTaskMem** verwendet wird.

Alle NAP-Funktionen zum Freigeben von Arbeitsspeicher gibt auch alle eingebetteten Zeiger frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






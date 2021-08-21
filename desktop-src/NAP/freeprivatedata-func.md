---
title: FreePrivateData-Funktion (NapUtil.h)
description: Gibt eine PrivateData-Datenstruktur frei.
ms.assetid: 94b3618e-224f-4801-94f3-2faa1a298ec0
keywords:
- NAP-Funktion "FreePrivateData"
topic_type:
- apiref
api_name:
- FreePrivateData
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c760a22ef377bd8d198ea3b913c6062e90338218a187cb9dec3af457a8a02493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134616"
---
# <a name="freeprivatedata-function"></a>FreePrivateData-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **FreePrivateData-Funktion** gibt eine [**PrivateData-Datenstruktur**](/windows/win32/api/naptypes/ns-naptypes-privatedata) frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreePrivateData(
  _In_ PrivateData *privateData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*privateData* \[ In\]
</dt> <dd>

Ein Zeiger [](/windows/win32/api/naptypes/ns-naptypes-privatedata) auf die privateData-Datenstruktur, die freigegeben werden soll.

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



 

 






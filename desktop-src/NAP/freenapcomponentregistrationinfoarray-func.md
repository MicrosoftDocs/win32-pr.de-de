---
title: FreeNapComponentRegistrationInfoArray-Funktion (NapUtil.h)
description: Gibt eine angegebene Anzahl von NapComponentRegistrationInfo-Datenstrukturen aus einem Array frei.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- NAP-Funktion "FreeNapComponentRegistrationInfoArray"
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d9d1aba35e7bf1ef332231836bd986b881f0e2dc995bc430075dfadf7bd482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940498"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a>FreeNapComponentRegistrationInfoArray-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **FreeNapComponentRegistrationInfoArray-Funktion** gibt eine angegebene Anzahl von [**NapComponentRegistrationInfo-Datenstrukturen**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) aus einem Array frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* \[ In\]
</dt> <dd>

Die Anzahl der [**NapComponentRegistrationInfo-Strukturen**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) in frei zu machende *Informationen.*

</dd> <dt>

*Info zu* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Array von [**NapComponentRegistrationInfo-Datenstrukturen,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die freigegeben werden sollen.

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



 

 






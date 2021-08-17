---
title: FreeSoH-Funktion (NapUtil.h)
description: Gibt eine SoH-Datenstruktur frei.
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- NAP-Funktion "FreeSoH"
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7e8236fcc8f0a2eaadd5b6f2ef81a393d68943d7fc5aeac5b00706ea06ec26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368682"
---
# <a name="freesoh-function"></a>FreeSoH-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **FreeSoH-Funktion** gibt eine **SoH-Datenstruktur** frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*soh* \[ In\]
</dt> <dd>

Ein Zeiger auf die [**frei**](/windows/win32/api/naptypes/ns-naptypes-soh) zu lassende SoH-Datenstruktur.

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



 

 






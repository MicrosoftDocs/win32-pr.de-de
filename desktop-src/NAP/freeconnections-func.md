---
title: FreeConnections-Funktion (NapUtil.h)
description: Gibt eine Verbindungsdatenstruktur frei.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- FreeConnections-Funktion NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258295df0b12f30d98825dd139eb51a7d1bc277417cf4d06bba9e811a00740db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940637"
---
# <a name="freeconnections-function"></a>FreeConnections-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **FreeConnections-Funktion** gibt eine [**Connections-Datenstruktur**](connections-struct.md) frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindungen* \[ In\]
</dt> <dd>

Ein Zeiger auf die frei zu lassende [**Connections-Struktur.**](connections-struct.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AllocConnections**](allocconnections-func.md)
</dt> </dl>

 

 






---
title: RPC_IF_HANDLE (rpcdce. h)
description: Der RPC \_ - \_ Datentyp "if-Handle" deklariert ein Schnittstellen handle.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956932"
---
# <a name="rpc_if_handle"></a>RPC- \_ if- \_ handle

Der RPC-Datentyp " **\_ if- \_ handle** " deklariert ein Schnittstellen handle.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Bemerkungen

Die RPC-Lauf Zeit Bibliothek verwendet Schnittstellen Handles für den Zugriff auf die Schnittstellen Spezifikations Datenstruktur. Der mittlerer l-Compiler erstellt automatisch eine Schnittstellen Spezifikations Datenstruktur aus jeder IDL-Datei und erstellt eine globale Variable des Typs RPC \_ if \_ Handle für die Schnittstellen Spezifikation.

Der mittlerer l-Compiler enthält ein Schnittstellen Handle in jeder für die Schnittstelle generierten Header Datei. Funktionen, die die Schnittstellen Spezifikation als Parameter erfordern, zeigen den Datentyp **RPC \_ if \_ handle** an. Die Form jedes Schnittstellen handle-namens lautet wie folgt:

-   *if-Name* \_ Clientithhandle (für den Client)
-   *if-Name* \_ Serverib handle (für den Server)

Der *if-Name-* Teil gibt den Schnittstellen Bezeichner in der IDL-Datei an.

Beispiel:

Hello \_ clientif handle

Hello \_ serverif handle

> [!Note]  
> Die maximale Länge des Schnittstellen handle-namens beträgt 31 Zeichen.

 

Da der " \_ clientibhandle"-und " \_ serveribhandle"-Teil der Namen 15 Zeichen erfordert, darf das *if-Name-* Element höchstens 16 Zeichen lang sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h (Include RPC. h)</dt> </dl> |



 

 






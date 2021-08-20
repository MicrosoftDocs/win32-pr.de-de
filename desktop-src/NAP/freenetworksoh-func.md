---
title: FreeNetworkSoH-Funktion (NapUtil.h)
description: Gibt eine NetworkSoH-Datenstruktur frei.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- FreeNetworkSoH-Funktion NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c2d3db800860295e0fa6173422ffeec0ca144550cc3ddfdf8a1ea391b6c6eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134751"
---
# <a name="freenetworksoh-function"></a>FreeNetworkSoH-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **FreeNetworkSoH-Funktion** gibt eine [**NetworkSoH-Datenstruktur**](/windows/win32/api/naptypes/ns-naptypes-networksoh) frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*networkSoh* \[ In\]
</dt> <dd>

Ein Zeiger auf die frei zu machende [**NetworkSoH-Datenstruktur.**](/windows/win32/api/naptypes/ns-naptypes-networksoh)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle vom NAP-System unterstützten COM-Schnittstellen verwenden standardmäßige COM-Speicherverwaltungsregeln und die COM-Speicherzuweisungen (**CoTaskMemAlloc** und **CoTaskMemFree**):

-   **In** werden Parameter vom Aufrufer zugeordnet und frei.
-   **Out-Parameter** werden vom Aufrufer zugeordnet und vom Aufrufer mithilfe von **CoTaskMem frei.**
-   **Ein-/Aus-Parameter** werden vom Aufrufer zugeordnet, vom Aufrufer frei und neu zugeordnet und schließlich vom Aufrufer mithilfe von **CoTaskMem frei.**

Alle NAP-Funktionen zum Freien von Arbeitsspeicher geben auch alle eingebetteten Zeiger frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






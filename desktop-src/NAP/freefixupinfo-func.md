---
title: FreeFixupInfo-Funktion (NapUtil.h)
description: Gibt eine FixupInfo-Datenstruktur frei.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- FreeFixupInfo-Funktion NAP
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
ms.openlocfilehash: 67c869123aadd5310a346dcf8e7a2184ec84f7e40500744cbaf610cbfc54db42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368870"
---
# <a name="freefixupinfo-function"></a>FreeFixupInfo-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **FreeFixupInfo-Funktion** gibt eine [**FixupInfo-Datenstruktur**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fixupInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf die frei zu verwendende [**FixupInfo-Datenstruktur.**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AllocFixupInfo**](allocfixupinfo-func.md)
</dt> </dl>

 

 






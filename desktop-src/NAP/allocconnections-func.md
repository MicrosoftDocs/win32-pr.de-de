---
title: AllocConnections-Funktion (NapUtil.h)
description: Weist Arbeitsspeicher für eine angegebene Anzahl von Verbindungsstrukturen zu.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- AllocConnections-Funktion NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf86a44b81ef12234fdac675aa55d36c5e1a336b4316382c3fd322cf0d6ba87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800205"
---
# <a name="allocconnections-function"></a>AllocConnections-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **AllocConnections-Funktion** weist Arbeitsspeicher für eine angegebene Anzahl von [**Connections-Strukturen**](connections-struct.md) zu.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindungen* \[ in, out\]
</dt> <dd>

Ein Zeiger auf ein Array neu zugeordneter [**Connections-Strukturen.**](connections-struct.md)

</dd> <dt>

*connectionsCount* \[ In\]
</dt> <dd>

Die Anzahl der Strukturen, die Verbindungen *zuteilen.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                   | Beschreibung                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ein ungültiges Argument wurde übergeben.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Das System befindet sich nicht im virtuellen Arbeitsspeicher. Fehler bei diesem Vorgang.<br/> |



 

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

[**FreeConnections**](freeconnections-func.md)
</dt> </dl>

 

 






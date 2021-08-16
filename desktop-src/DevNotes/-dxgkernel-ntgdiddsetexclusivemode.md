---
description: Benachrichtigt den Treiber, wenn eine Microsoft DirectDraw-Anwendung in den oder aus dem exklusiven Modus wechselt.
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: NtGdiDdSetExclusiveMode-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 00b158c44aff185dd478aa9806e6fa9023f6bedb33127250e615f680e5a6a9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827991"
---
# <a name="ntgdiddsetexclusivemode-function"></a>NtGdiDdSetExclusiveMode-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Benachrichtigt den Treiber, wenn eine Microsoft DirectDraw-Anwendung in den oder aus dem exklusiven Modus wechselt.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für zuvor erstelltes DirectDraw-Objekt im Kernelmodus.

</dd> <dt>

*puSetExclusiveModeData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**\_ SETEXCLUSIVEMODEDATA-DD-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) die die Benachrichtigungsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdSetExclusiveMode** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DDHAL-TREIBER \_ BEHANDELT**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 

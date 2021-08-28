---
description: Fragt den Status des letzten Renderingvorgangs auf der angegebenen Oberfläche ab.
ms.assetid: bc7f8f84-119e-4c09-87f5-6b122e9f9821
title: NtGdiDdQueryMoCompStatus-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryMoCompStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8864573e3e84b2e09fb28ad997aab004dfe88916eb8af5f0ee8b3d47437188e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088010"
---
# <a name="ntgdiddquerymocompstatus-function"></a>NtGdiDdQueryMoCompStatus-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Fragt den Status des letzten Renderingvorgangs auf der angegebenen Oberfläche ab.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdQueryMoCompStatus(
  _In_    HANDLE                    hMoComp,
  _Inout_ PDD_QUERYMOCOMPSTATUSDATA puQueryMoCompStatusData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMoComp* \[ In\]
</dt> <dd>

Zeiger auf eine [**DD \_ MOTIONCOMP \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) die eine Beschreibung der angeforderten Bewegungskompensierung enthält.

</dd> <dt>

*puQueryMoCompStatusData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ QUERYMOCOMPSTATUSDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_querymocompstatusdata) die die zum Abfragen des Status erforderlichen Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdQueryMoCompStatus** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie im Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 

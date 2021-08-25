---
description: Führt eine Bitblockübertragung aus.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: NtGdiDdBlt-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f0f4ae51663e9d1c398c34708520047f43288c1f571458a879e262ec9fca025d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911955"
---
# <a name="ntgdiddblt-function"></a>NtGdiDdBlt-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Führt eine Bitblockübertragung aus.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurfaceDest* \[ In\]
</dt> <dd>

Handle für eine [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die Oberfläche beschreibt, auf der blitt werden soll.

</dd> <dt>

*hSurfaceSrc* \[ In\]
</dt> <dd>

Handle für eine [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die Quelloberfläche beschreibt.

</dd> <dt>

*puBltData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ BLTDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) die die Informationen enthält, die der Treiber zum Ausführen des Blits benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdBlt gibt** einen der folgenden Rückrufcodes zurück.



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

 

 

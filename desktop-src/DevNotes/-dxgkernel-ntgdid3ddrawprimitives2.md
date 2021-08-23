---
description: Rendert Primitive und gibt den aktualisierten Renderzustand zurück.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: NtGdiD3DDrawPrimitives2-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8d3964a9946da37d211aab0e5949cff5e09a40dcc18607aabb3a0c13c37acfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833660"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>NtGdiD3DDrawPrimitives2-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Rendert Primitive und gibt den aktualisierten Renderzustand zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCmdBuf* \[ In\]
</dt> <dd>

Handle für die [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die DirectDraw-Oberfläche identifiziert, die die Befehlsdaten enthält.

</dd> <dt>

*hVBuf* \[ In\]
</dt> <dd>

Handle für die [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die DirectDraw-Oberfläche identifiziert, die die Scheitelpunktdaten enthält.

</dd> <dt>

*pded* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**D3DNTHAL \_ DRAWPRIMITIVES2DATA-Struktur,**](/windows-hardware/drivers/ddi/) die die Informationen enthält, die der Treiber zum Rendern eines oder mehrerer Primitive benötigt.

</dd> <dt>

*pfpVidMemCmd* \[ in, out\]
</dt> <dd>

Neuer Zeiger auf den Videospeicher, wenn der Treiber den Befehlspuffer getauscht hat.

</dd> <dt>

*pdwSizeCmd* \[ in, out\]
</dt> <dd>

Gibt die Mindestanzahl von Bytes an, um die der Treiber den Puffer des Austauschbefehls erhöhen muss.

</dd> <dt>

*pfpVidMemVtx* \[ in, out\]
</dt> <dd>

Neuer Zeiger auf den Videospeicher, wenn der Treiber den Scheitelpunktpuffer getauscht hat.

</dd> <dt>

*pdwSizeVtx* \[ in, out\]
</dt> <dd>

Gibt die Mindestanzahl von Bytes an, die der Treiber für den Vertexpuffer für den Austausch zuordnen muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiD3DDrawPrimitives2** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

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

 

 

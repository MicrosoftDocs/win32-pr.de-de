---
description: Rendert primitive und gibt den aktualisierten renderzustand zurück.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: NtGdiD3DDrawPrimitives2-Funktion (ntgdi. h)
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
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041371"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>NtGdiD3DDrawPrimitives2-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Rendert primitive und gibt den aktualisierten renderzustand zurück.

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

*hcmdbuf* \[ in\]
</dt> <dd>

Handle für die [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-Oberfläche mit den Befehlsdaten identifiziert.

</dd> <dt>

*hvbuf* \[ in\]
</dt> <dd>

Handle für die [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die DirectDraw-Oberfläche identifiziert, die die Scheitelpunkt Daten enthält.

</dd> <dt>

*pded* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) -Struktur, die die Informationen enthält, die der Treiber zum Rendering von mindestens einem primitiv benötigt.

</dd> <dt>

*pfpvidmemcmd* \[ in, out\]
</dt> <dd>

Neuer Zeiger auf den Videospeicher, wenn der Treiber den Befehls Puffer ausgetauscht hat.

</dd> <dt>

*pdwsizecmd* \[ in, out\]
</dt> <dd>

Gibt die Mindestanzahl von Bytes an, um die der Treiber den Austausch Befehls Puffer erhöhen muss.

</dd> <dt>

*pfpvidmemvtx* \[ in, out\]
</dt> <dd>

Neuer Zeiger auf den Videospeicher, wenn der Treiber den Vertex-Puffer ausgetauscht hat.

</dd> <dt>

*pdwsizevtx* \[ in, out\]
</dt> <dd>

Gibt die Mindestanzahl von Bytes an, die der Treiber für den Vertex-Austausch Puffer zuordnen muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiD3DDrawPrimitives2** gibt einen der folgenden Rückruf Codes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ddhal- \_ Treiber \_ behandelt**</dt> </dl>    | Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**ddhal- \_ Treiber \_ nothandled**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 

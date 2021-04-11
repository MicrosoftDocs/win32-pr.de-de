---
description: Führt eine Bitblock Übertragung aus.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Ntgdiddblt-Funktion (ntgdi. h)
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
ms.openlocfilehash: 86249a8ff1069bc0875aad3fcca576ef78b9db68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126763"
---
# <a name="ntgdiddblt-function"></a>Ntgdiddblt-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Führt eine Bitblock Übertragung aus.

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

*hsurfacedest* \[ in\]
</dt> <dd>

Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Oberfläche beschreibt, auf der Blit werden soll.

</dd> <dt>

*hsurfakesrc* \[ in\]
</dt> <dd>

Handle für eine [**\_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die die Quell Oberfläche beschreibt.

</dd> <dt>

*publtdata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ bltdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) -Struktur, die die Informationen enthält, die der Treiber zum Durchführen des Blit benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddblt** gibt einen der folgenden Rückruf Codes zurück.



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

 

 

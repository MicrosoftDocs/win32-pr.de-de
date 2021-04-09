---
description: Erstellt eine Microsoft Direct3D-Oberfläche aus einer Microsoft DirectDraw-Oberfläche und ordnet ihr einen angeforderten handle-Wert zu.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Ntgdiddkreatesurfaceex-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125941"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>Ntgdiddkreatesurfaceex-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Erstellt eine Microsoft Direct3D-Oberfläche aus einer Microsoft DirectDraw-Oberfläche und ordnet ihr einen angeforderten handle-Wert zu.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdraw* \[ in\]
</dt> <dd>

Handle für das von der Anwendung erstellte DirectDraw-Objekt.

</dd> <dt>

*hsurface* \[ in\]
</dt> <dd>

Handle für die DirectDraw-Oberfläche, die für Direct3D erstellt werden soll. Diese Handles sind innerhalb jeder anderen [**DD \_ DirectDraw- \_ lokalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) Struktur eindeutig.

</dd> <dt>

*dwsurfakehandle* \[ in\]
</dt> <dd>

Handle für eine DD-Struktur von " [**\_ foatesurfaceexdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) ", die die Informationen enthält, die der Treiber zum Erstellen der Oberfläche benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddkreatesurfaceex** gibt einen der folgenden Rückruf Codes zurück.



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

 

 

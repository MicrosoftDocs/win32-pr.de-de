---
description: Erstellt eine Kernel seitige Darstellung des Microsoft DirectDraw-Objekts.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Ntgdiddkreatedirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125942"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a>Ntgdiddkreatedirectdrawobject-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Erstellt eine Kernel seitige Darstellung des Microsoft DirectDraw-Objekts.

## <a name="syntax"></a>Syntax


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ in\]
</dt> <dd>

Alle DC-Anzeigegeräte, für die das DirectDraw-Objekt erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Funktion ein Handle für die Objektdarstellung im Kernelmodus zurück. Andernfalls wird **null** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten. Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**Ddkreatedirectdrawobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 

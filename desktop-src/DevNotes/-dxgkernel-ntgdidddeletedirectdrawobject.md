---
description: Zerstört ein zuvor erstelltes Microsoft DirectDraw-Geräte Objekt im Kernel Modus.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Ntgdidddeletedirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125936"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>Ntgdidddeletedirectdrawobject-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Zerstört ein zuvor erstelltes Microsoft DirectDraw-Geräte Objekt im Kernel Modus.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdrawlocal* 
</dt> <dd>

Handle für das DirectDraw-Geräte Objekt im Kernel Modus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.

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

[**Ntgdiddkreatedirectdrawobject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**Dddeletedirectdrawobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 

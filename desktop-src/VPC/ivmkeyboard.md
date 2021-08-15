---
title: IVMKeyboard-Schnittstelle (VPCCOMInterfaces.h)
description: Steuert das Tastaturgerät auf einem virtuellen Computer. Das IVMKeyboard für einen virtuellen Computer kann mithilfe der EIGENSCHAFT IVMVirtualMachine Keyboard abgerufen werden.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- IVMKeyboard-Schnittstelle Virtueller PC
- IVMKeyboard-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7284c4e2bb164cd53c8a34357c881ed096f342ae2c2230422985fac4c1fdae9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344797"
---
# <a name="ivmkeyboard-interface"></a>IVMKeyboard-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Steuert das Tastaturgerät auf einem virtuellen Computer. Das **IVMKeyboard** für einen virtuellen Computer kann mithilfe der [**IVMVirtualMachine::Keyboard-Eigenschaft abgerufen**](ivmvirtualmachine-keyboard.md) werden.

## <a name="members"></a>Member

Die **IVMKeyboard-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMKeyboard** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMKeyboard-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Ispressed**](ivmkeyboard-ispressed.md)                   | Bestimmt, ob der angegebene Schlüssel nicht mehr verwendet werden kann.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simuliert, dass eine Taste gedrückt und dann freigegeben wird.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simuliert, dass eine Taste gedrückt wird.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simuliert, dass ein Schlüssel freigegeben wird.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gasttyp eingedrungen werden.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die im Gasttyp verwendet werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IVMKeyboard-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp           | BESCHREIBUNG                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob dieses Objekt die exklusive Kontrolle über das Tastaturgerät des virtuellen Computers hat.<br/> |



 

## <a name="remarks"></a>Hinweise

Schlüssel können auf verschiedene Weise in den virtuellen Computer typisierten werden. Verwenden Sie zum Eingeben einer normalen ASCII-Sequenz von Zeichen [**die TypeAsciiText-Methode.**](ivmkeyboard-typeasciitext.md) Wenn mehr Flexibilität erforderlich ist, verfügt **IVMKeyboard** über mehrere Methoden, die für die Verwendung mit den Schlüsselcodes in der folgenden Liste entworfen wurden. Die [**TypeKeySequence-Methode**](ivmkeyboard-typekeysequence.md) kann eine durch Trennzeichen getrennte Zeichenfolge von Schlüsselcodes akzeptieren, die auf dem virtuellen Computer in der reihenfolgenweise gedrückt und freigegeben werden. Zusätzlich zu diesen Schlüsselcodes können die Schlüsselwörter UP und DOWN verwendet werden, um zu erzwingen, dass eine Taste nur gedrückt oder nur freigegeben wird. Die Schlüsselwörter UP und DOWN gelten nur für den Schlüsselcode, der direkt auf das Schlüsselwort folgt.

Um zu vermeiden, dass mehrere Skripts, Anwendungen oder Benutzer gleichzeitig versuchen, auf dasselbe Tastaturgerät zu zugreifen, legen Sie die [**HasExclusiveAccess-Eigenschaft**](ivmkeyboard-hasexclusiveaccess.md) auf **TRUE fest.** Wenn ein Prozess exklusiven Zugriff erlangt, werden alle Versuche anderer Prozesse, Eingaben an das Tastaturgerät zu senden, ignoriert, bis der exklusive Zugriff freigegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard ist als 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4 definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Virtuelle PC-Schnittstellen](virtual-pc-interfaces.md)
</dt> <dt>

[Schlüsselsequenzen](key-sequences.md)
</dt> </dl>

 


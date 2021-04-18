---
title: Ivmkeyboard-Schnittstelle (vpccominterfaces. h)
description: Steuert das Tastatur Gerät innerhalb einer virtuellen Maschine. Die ivmkeyboard für eine virtuelle Maschine kann mithilfe der ivmvirtualmachine-Tastatur Eigenschaft abgerufen werden.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Ivmkeyboard Interface Virtual PC
- Virtueller Computer für ivmkeyboard Interface, beschrieben
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
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340374"
---
# <a name="ivmkeyboard-interface"></a>Ivmkeyboard-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Steuert das Tastatur Gerät innerhalb einer virtuellen Maschine. Die **ivmkeyboard** für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine:: Keyboard**](ivmvirtualmachine-keyboard.md) -Eigenschaft abgerufen werden.

## <a name="members"></a>Member

Die **ivmkeyboard** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmkeyboard** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmkeyboard** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Igestreout**](ivmkeyboard-ispressed.md)                   | Bestimmt, ob der angegebene Schlüssel nicht angezeigt wird.<br/>                      |
| [**Pressandreleasekey**](ivmkeyboard-pressandreleasekey.md) | Simuliert, dass eine Taste gedrückt und anschließend freigegeben wird.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simuliert, dass eine Taste gedrückt wird.<br/>                                |
| [**Releasekey**](ivmkeyboard-releasekey.md)                 | Simuliert einen Schlüssel, der freigegeben wird.<br/>                                    |
| [**Tybäuerciitext**](ivmkeyboard-typeasciitext.md)           | Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.<br/>       |
| [**Typekeysequence**](ivmkeyboard-typekeysequence.md)       | Simuliert eine durch Trennzeichen getrennte Liste mit Schlüsseln, die in den Gast eingegeben werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmkeyboard** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp           | BESCHREIBUNG                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Hasexclusiveaccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob dieses-Objekt über eine exklusive Kontrolle über das Tastatur Gerät der virtuellen Maschine verfügt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Schlüssel können auf verschiedene Arten in den virtuellen Computer eingegeben werden. Verwenden Sie die [**tybäuerciitext**](ivmkeyboard-typeasciitext.md) -Methode, um eine normale ASCII-Zeichenfolge einzugeben. Wenn mehr Flexibilität erforderlich ist, verfügt **ivmkeyboard** über mehrere Methoden, die für die Verwendung mit den Schlüsselcodes in der folgenden Liste konzipiert sind. Die [**typekeysequence**](ivmkeyboard-typekeysequence.md) -Methode kann eine durch Trennzeichen getrennte Zeichenfolge von Schlüsselcodes akzeptieren, die in der angegebenen Reihenfolge innerhalb des virtuellen Computers gedrückt und freigegeben werden. Zusätzlich zu diesen Schlüsselcodes können die Schlüsselwörter "hoch" und "nach unten" verwendet werden, um zu erzwingen, dass eine Taste gedrückt wird oder nur freigegeben wird. Die Schlüsselwörter "up" und "Down" gelten nur für den Schlüsselcode, der direkt auf das Schlüsselwort

Um zu vermeiden, dass mehrere Skripts, Anwendungen oder Benutzer gleichzeitig versuchen, auf dasselbe Tastatur Gerät zuzugreifen, legen Sie die [**hasexclusiveaccess**](ivmkeyboard-hasexclusiveaccess.md) -Eigenschaft auf **true** fest. Wenn exklusiver Zugriff von einem Prozess abgerufen wird, werden alle Versuche anderer Prozesse, Eingaben an das Tastatur Gerät zu senden, ignoriert, bis der exklusive Zugriff aufgehoben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Virtual PC-Schnittstellen](virtual-pc-interfaces.md)
</dt> <dt>

[Schlüsselsequenzen](key-sequences.md)
</dt> </dl>

 


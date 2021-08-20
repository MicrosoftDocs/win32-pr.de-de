---
title: IVMKeyboard TypeKeySequence-Methode (VPCCOMInterfaces.h)
description: Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die typiert werden.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- 'TypeKeySequence-Methode : Virtueller PC'
- TypeKeySequence-Methode Virtual PC, IVMKeyboard-Schnittstelle
- IVMKeyboard-Schnittstelle Virtueller PC, TypeKeySequence-Methode
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565d31d04a31f72ea25b3477fb91d53d252f6173eec8bc2f40133db38eeb1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998860"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>IVMKeyboard::TypeKeySequence-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die typiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*keySequence* \[ In\]
</dt> <dd>

Die durch Trennzeichen getrennte Sequenz von Schlüsselcodes, die typiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>      | Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |



 

## <a name="remarks"></a>Hinweise

Eine Tastensequenzzeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüsselbezeichnern, die verwendet werden, um die Tastenkombination und die Freigabesequenz einer STANDARDTASTATUR (U.S. 101) zu simulieren.

Wenn ein Schlüsselbezeichner in der Zeichenfolge ohne vorangehenden Modifizierer angezeigt wird, wird ein per Taste gedrückter Code an die Sitzung des virtuellen Computers gesendet, unmittelbar gefolgt von dem entsprechenden, von der Taste freigegebenen Code. Schlüsselmodifizierer können verwendet werden, um dieses Verhalten zu ändern.

Der DOWN-Modifizierer sendet z. B. den gedrückten Code für den folgenden Schlüsselbezeichner, ohne den code freigelassenen Schlüssel zu senden. Dies ist nützlich, um STRG-, ALT- und UMSCHALTTASTEn zu simulieren, wenn sie gedrückt gehalten werden, während andere Tasten gesendet werden. Um den Schlüssel frei zu geben, muss er zusammen mit einem vorangehenden UP-Modifizierer erneut in die Schlüsselzeichenfolge eingeschlossen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard ist als 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> <dt>

[Schlüsselsequenzen](key-sequences.md)
</dt> </dl>

 


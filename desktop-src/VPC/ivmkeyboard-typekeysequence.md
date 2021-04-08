---
title: Ivmkeyboard typekeysequence-Methode (vpccominterfaces. h)
description: Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die eingegeben werden.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Typekeysequence-Methode Virtual PC
- Typekeysequence-Methode Virtual PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, typekeysequence-Methode
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
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957122"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>Ivmkeyboard:: typekeysequence-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simuliert eine durch Trennzeichen getrennte Liste von Schlüsseln, die eingegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*keysequence* \[ in\]
</dt> <dd>

Die durch Trennzeichen getrennte Sequenz von Schlüsselcodes, die eingegeben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                                      |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>      | Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |



 

## <a name="remarks"></a>Bemerkungen

Eine Schlüssel Sequenz Zeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüssel Bezeichnerzeichen, die verwendet werden, um die Tastenkombination und die releasesequenz einer Standardtastatur des US-amerikanischen 101-Schlüssels zu simulieren.

Wenn ein Schlüssel Bezeichner in der Zeichenfolge ohne einen vorangehenden Modifizierer angezeigt wird, wird ein mit Schlüsseln gedrückter Code an die Sitzung der virtuellen Maschine gesendet, gefolgt von dem zugehörigen Schlüsselcode. Schlüsselmodifizierer können verwendet werden, um dieses Verhalten zu ändern.

Der Down-Modifizierer sendet z. b. den Schlüssel gesteuerten Code für den folgenden Schlüssel Bezeichner, ohne den Schlüssel freigegebenen Code zu senden. Dies ist nützlich zum Simulieren von STRG-, alt-und Umschalttaste, wenn Sie gedrückt werden, während andere Schlüssel gesendet werden. Um den Schlüssel freizugeben, muss er erneut in die Schlüssel Zeichenfolge eingefügt werden, zusammen mit einem vorangehenden Modifizierer.

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

[**Ivmkeyboard**](ivmkeyboard.md)
</dt> <dt>

[Schlüsselsequenzen](key-sequences.md)
</dt> </dl>

 


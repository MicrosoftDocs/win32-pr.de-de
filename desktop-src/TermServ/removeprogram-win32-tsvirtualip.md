---
title: Removeprogram-Methode der Win32_TSVirtualIP-Klasse (bmolface. h)
description: Entfernt ein Programm aus der Liste der Programme, die die IP-Virtualisierung verwenden.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Removeprogram-Methode Remotedesktopdienste
- Removeprogram-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, removeprogram-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743625"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a>Removeprogram-Methode der Win32- \_ Klasse "tvirtualip"

Entfernt ein Programm aus der Liste der Programme, die die IP-Virtualisierung verwenden.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Programpath* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Pfad und der Dateiname des Programms, das aus der Liste entfernt werden soll. Wenn das Programm nicht gefunden wird, wird ein Fehler zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Header<br/>                   | <dl> <dt>Bmolface. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ virtualialip**](win32-tsvirtualip.md)
</dt> </dl>

 

 






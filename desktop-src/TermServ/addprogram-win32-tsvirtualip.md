---
title: Addprogram-Methode der Win32_TSVirtualIP-Klasse (bmolface. h)
description: Fügt der Liste der Programme, die die IP-Virtualisierung verwenden, ein Programm hinzu.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Addprogram-Methode Remotedesktopdienste
- Addprogram-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, addprogram-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740768"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a>Addprogram-Methode der Win32- \_ Klasse "tvirtualip"

Fügt der Liste der Programme, die die IP-Virtualisierung verwenden, ein Programm hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Programpath* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Pfad und der Dateiname des Programms, das der Liste hinzugefügt werden soll.

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

 

 






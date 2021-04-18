---
title: Setvirtualipmode-Methode der Win32_TSVirtualIP-Klasse
description: Legt den Wert der virtualipmode-Eigenschaft fest.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Setvirtualipmode-Methode Remotedesktopdienste
- Setvirtualipmode-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, setvirtualipmode-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344685"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Setvirtualipmode-Methode der Win32- \_ Klasse "tvirtualip"

Legt den Wert der **virtualipmode** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Virtualisierungsmodus* \[ in\]
</dt> <dd>

Typ: **UInt32**

Gibt an, welcher IP-Virtualisierungsmodus auf dem Server verwendet wird. Dies kann einer der folgenden Werte sein:

<dt>

0
</dt> <dd>

Der IP-Virtualisierungsmodus ist pro Sitzung.

</dd> <dt>

1
</dt> <dd>

Der IP-Virtualisierungsmodus ist pro Benutzer.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ virtualialip**](win32-tsvirtualip.md)
</dt> </dl>

 

 






---
title: Setvirtualipactive-Methode der Win32_TSVirtualIP-Klasse
description: Legt den Wert der virtualipactive-Eigenschaft fest.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Setvirtualipactive-Methode Remotedesktopdienste
- Setvirtualipactive-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, setvirtualipactive-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956664"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Setvirtualipactive-Methode der Win32- \_ Klasse "tvirtualip"

Legt den Wert der **virtualipactive** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Virtualipactive* \[ in\]
</dt> <dd>

Typ: **UInt32**

Gibt an, ob die IP-Virtualisierung auf dem Server aktiv ist. Dies kann einer der folgenden Werte sein:

<dt>

Null
</dt> <dd>

Die IP-Virtualisierung ist nicht aktiv.

</dd> <dt>

ungleich NULL
</dt> <dd>

Die IP-Virtualisierung ist aktiv.

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

 

 






---
title: SetVirtualIPActive-Methode der Win32_TSVirtualIP-Klasse
description: Legt den VirtualIPActive-Eigenschaftswert fest.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- SetVirtualIPActive-Methode Remotedesktopdienste
- SetVirtualIPActive-Methode Remotedesktopdienste , Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste , SetVirtualIPActive-Methode
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
ms.openlocfilehash: 2ab43a007a2a8b04e91d5225e648d5667a87c468cbd52c005d85f4ba6496c919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850919"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>SetVirtualIPActive-Methode der Win32 \_ TSVirtualIP-Klasse

Legt den **VirtualIPActive-Eigenschaftswert** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VirtualIPActive* \[ In\]
</dt> <dd>

Typ: **uint32**

Gibt an, ob die IP-Virtualisierung auf dem Server aktiv ist. Dies kann einer der folgenden Werte sein.

<dt>

Null
</dt> <dd>

DIE IP-Virtualisierung ist nicht aktiv.

</dd> <dt>

Nonzero
</dt> <dd>

IP-Virtualisierung ist aktiv.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 






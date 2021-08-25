---
title: SetLoadBalancingState-Methode der Win32_TSSessionDirectory Klasse
description: Legt den Wert fest, um anzugeben, ob der Server am Lastenausgleich Remotedesktopverbindung Broker (RD-Verbindungsbroker) beteiligt ist.
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- SetLoadBalancingState-Remotedesktopdienste
- SetLoadBalancingState-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory klasse Remotedesktopdienste , SetLoadBalancingState-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d539f07c97e4e5b92152190a7bb38a8132d31a73daf08de8f140a39f67efdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987950"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>SetLoadBalancingState-Methode der Win32 \_ TSSessionDirectory-Klasse

Legt den Wert fest, um anzugeben, ob der Server am Lastenausgleich Remotedesktopverbindung Broker (RD-Verbindungsbroker) beteiligt ist.

## <a name="syntax"></a>Syntax


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StateValue* \[ In\]
</dt> <dd>

Typ: **uint32**

Gibt an, ob der Server am Lastenausgleich des RD-Verbindungsbrokers beteiligt ist.

<dt>

0
</dt> <dd>

Der Server nimmt nicht am Lastenausgleich des RD-Verbindungsbrokers teil.

</dd> <dt>

1
</dt> <dd>

Der Server nimmt am Lastenausgleich des RD-Verbindungsbrokers teil.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Der Server muss einer Farm im RD-Verbindungsbroker beigetreten sein.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


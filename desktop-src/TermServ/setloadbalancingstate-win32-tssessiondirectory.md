---
title: Setloadbalancingstate-Methode der Win32_TSSessionDirectory-Klasse
description: Legt den Wert fest, mit dem angegeben wird, ob der Server am Remotedesktopverbindung Broker-Lastenausgleich (RD-Verbindungsbroker) beteiligt ist.
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Setloadbalancingstate-Methode Remotedesktopdienste
- Setloadbalancingstate-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, setloadbalancingstate-Methode
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
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341371"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Setloadbalancingstate-Methode der Win32- \_ Klasse "tssessiondirectory"

Legt den Wert fest, mit dem angegeben wird, ob der Server am Remotedesktopverbindung Broker-Lastenausgleich (RD-Verbindungsbroker) beteiligt ist.

## <a name="syntax"></a>Syntax


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ in\]
</dt> <dd>

Typ: **UInt32**

Gibt an, ob der Server an RD-Verbindungsbroker Lastenausgleich beteiligt ist.

<dt>

0
</dt> <dd>

Der Server wird nicht an RD-Verbindungsbroker Lastenausgleich beteiligt.

</dd> <dt>

1
</dt> <dd>

Der Server wird an RD-Verbindungsbroker Lastenausgleich beteiligt.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Server muss in RD-Verbindungsbroker einer Farm hinzugefügt werden.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


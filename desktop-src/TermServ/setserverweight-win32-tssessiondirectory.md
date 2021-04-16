---
title: Setserverweight-Methode der Win32_TSSessionDirectory-Klasse
description: Legt den Server Gewichtungswert für den Lastenausgleich von Remotedesktopverbindung Broker (RD-Verbindungsbroker) fest.
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Setserverweight-Methode Remotedesktopdienste
- Setserverweight-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, setserverweight-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477715"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Setserverweight-Methode der Win32- \_ Klasse "tssessiondirectory"

Legt den Server Gewichtungswert für den Lastenausgleich von Remotedesktopverbindung Broker (RD-Verbindungsbroker) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Serverweightvalue* \[ in\]
</dt> <dd>

Typ: **UInt32**

Der Server Gewichtungswert. Der gültige Bereich liegt zwischen 1 und 10000.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist der Server Gewichtungswert in der Benutzeroberfläche Remotedesktopdienste Konfiguration 100. Die Server Gewichtung ist relativ. Wenn Sie einen Server mit einem Wert von 100 und einem Wert von 200 zuweisen, erhält der Server mit der relativen Gewichtung 200 die doppelte Anzahl von Sitzungen.

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

 


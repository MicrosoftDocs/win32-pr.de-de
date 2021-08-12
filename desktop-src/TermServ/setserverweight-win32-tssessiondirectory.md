---
title: SetServerWeight-Methode der Win32_TSSessionDirectory-Klasse
description: Legt den Servergewichtungswert für Remotedesktopverbindung Broker-Lastenausgleich (RD-Verbindungsbroker) fest.
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- SetServerWeight-Methode Remotedesktopdienste
- SetServerWeight-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste , SetServerWeight-Methode
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
ms.openlocfilehash: 96d8c9af7995f2d42f02075fde8ae43f4b5f5e9a5ccb7d3fa6f4635cb9645464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604629"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>SetServerWeight-Methode der Win32 \_ TSSessionDirectory-Klasse

Legt den Servergewichtungswert für Remotedesktopverbindung Broker-Lastenausgleich (RD-Verbindungsbroker) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerWeightValue* \[ In\]
</dt> <dd>

Typ: **uint32**

Der Wert der Servergewichtung. Der gültige Bereich liegt zwischen 1 und 10.000.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In der Benutzeroberfläche von Remotedesktopdienste Configuration ist der Wert für die Servergewichtung standardmäßig 100. Die Servergewichtung ist relativ. Wenn Sie also einem Server den Wert 100 und einen Wert von 200 zuweisen, erhält der Server mit einer relativen Gewichtung von 200 die doppelte Anzahl von Sitzungen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


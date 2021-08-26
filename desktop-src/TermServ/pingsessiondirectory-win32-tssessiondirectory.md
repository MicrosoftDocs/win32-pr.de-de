---
title: PingSessionDirectory-Methode der Win32_TSSessionDirectory Klasse
description: Überprüft, ob Remotedesktopverbindung Broker-Server (RD-Verbindungsbroker) verfügbar ist.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- PingSessionDirectory-Remotedesktopdienste
- PingSessionDirectory-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory klasse Remotedesktopdienste , PingSessionDirectory-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26afbf26ab637dd58d8249ee822e152feefd948079f97c6e0adb876b4c7f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988840"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a>PingSessionDirectory-Methode der Win32 \_ TSSessionDirectory-Klasse

Überprüft, ob Remotedesktopverbindung Broker-Server (RD-Verbindungsbroker) verfügbar ist.

## <a name="syntax"></a>Syntax


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerName* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Name des RD-Verbindungsbrokerservers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


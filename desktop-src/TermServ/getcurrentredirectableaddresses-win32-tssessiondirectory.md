---
title: GetCurrentRedirectableAddresses-Methode der Win32_TSSessionDirectory-Klasse
description: Ruft die derzeit konfigurierte Liste der dns-berechtigten Adressen ab, die für die Umleitung verwendet werden können.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- GetCurrentRedirectableAddresses-Methode Remotedesktopdienste
- GetCurrentRedirectableAddresses-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste , GetCurrentRedirectableAddresses-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35033decd836cda3f8a9ca3100a22cd16b6ec87a284ce3c012db382fa15da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010150"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>GetCurrentRedirectableAddresses-Methode der Win32 \_ TSSessionDirectory-Klasse

Ruft die derzeit konfigurierte Liste der dns-berechtigten Adressen ab, die für die Umleitung verwendet werden können.

## <a name="syntax"></a>Syntax


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fTokenRedirection* \[ out\]
</dt> <dd>

Typ: **uint32**

Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.

</dd> <dt>

*IPAddresses* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein Array der derzeit konfigurierten DNS-berechtigten IP-Adressen, die für die Umleitung verwendet werden können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück. andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


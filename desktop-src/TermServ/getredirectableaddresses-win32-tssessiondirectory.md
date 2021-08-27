---
title: GetRedirectableAddresses-Methode der Win32_TSSessionDirectory-Klasse
description: Ruft die gesamte Liste der dns-berechtigten Adressen ab.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- GetRedirectableAddresses-Methode Remotedesktopdienste
- GetRedirectableAddresses-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste , GetRedirectableAddresses-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff3e5dda8459361855c6ff2b287b71cbe02136b906e7defc816d4e7df727a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010104"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>GetRedirectableAddresses-Methode der Win32 \_ TSSessionDirectory-Klasse

Ruft die gesamte Liste der dns-berechtigten Adressen ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fTokenRedirection* \[ In\]
</dt> <dd>

Typ: **uint32**

Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.

</dd> <dt>

*IPAddresses* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Die gesamte Liste der IP-Adressen, die für die Umleitung verfügbar sind.

</dd> <dt>

*AdapterNames* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Die Liste der Netzwerkadapternamen, die den Adressen zugeordnet sind, die für die Umleitung verfügbar sind.

</dd> <dt>

*NetConName* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Die Liste der Netzwerkverbindungsnamen, die den Adressen zugeordnet sind, die für die Umleitung verfügbar sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


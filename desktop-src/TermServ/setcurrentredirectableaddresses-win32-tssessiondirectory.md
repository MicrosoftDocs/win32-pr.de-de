---
title: SetCurrentRedirectableAddresses-Methode der Win32_TSSessionDirectory Klasse
description: Legt die konfigurierte Liste der DNS-fähigen Adressen fest, die für die Umleitung verwendet werden können.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- SetCurrentRedirectableAddresses-Remotedesktopdienste
- SetCurrentRedirectableAddresses-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory klasse Remotedesktopdienste , SetCurrentRedirectableAddresses-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf1e9ab7b385111ccf91af9b4e3d6ed8bed0191f2d044c02a41705dbbc4f781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756100"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>SetCurrentRedirectableAddresses-Methode der Win32 \_ TSSessionDirectory-Klasse

Die **SetCurrentRedirectableAddresses-Methode** legt die konfigurierte Liste der DNS-berechtigten Adressen fest, die für die Umleitung verwendet werden können.

## <a name="syntax"></a>Syntax


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fTokenRedirection* \[ In\]
</dt> <dd>

Typ: **uint32**

Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.

</dd> <dt>

*IPAddresses* \[ In\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein Array von Zeichenfolgen, das die Liste der DNS-fähigen IP-Adressen darstellt, die für die Umleitung verwendet werden können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück. andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


---
title: SetMaxXResolution-Methode der Win32_TSClientSetting-Klasse
description: Legt die MaxXResolution-Eigenschaft fest.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- SetMaxXResolution-Methode Remotedesktopdienste
- SetMaxXResolution-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , SetMaxXResolution-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759a674e2b283d18caf1cc4d1b2f3e3ecae786dc76f9acc222f47dd8daf385de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000510"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a>SetMaxXResolution-Methode der Win32 \_ TSClientSetting-Klasse

Legt die **MaxXResolution-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MaxXResolution* \[ In\]
</dt> <dd>

Die neue maximale X-Auflösung, die vom Server unterstützt wird. Der Mindestwert ist 200 und der Höchstwert 4096.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 






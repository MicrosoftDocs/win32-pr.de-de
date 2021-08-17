---
title: SetClientProperty-Methode der Win32_TSClientSetting-Klasse
description: Die SetClientProperty-Methode legt die LPTPortMapping-, COMPortMapping-, AudioMapping-, ClipboardMapping-, DriveMapping- oder WindowsPrinterMapping-Eigenschaft für die -Klasse fest.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- SetClientProperty-Methode Remotedesktopdienste
- SetClientProperty-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , SetClientProperty-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017a771022e0f5edc7d4abe22501fc8dfadc006e01ed2642f95f9c39f101eef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127016"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a>SetClientProperty-Methode der Win32 \_ TSClientSetting-Klasse

Die **SetClientProperty-Methode** legt die **LPTPortMapping-,** **COMPortMapping-,** **AudioMapping-,** **ClipboardMapping-,** **DriveMapping-** oder **WindowsPrinterMapping-Eigenschaft** für die -Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyName* \[ In\]
</dt> <dd>

Gibt die Clienteigenschaft an, die von der Methode festgelegt wird.

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**


</dt> <dd>

Die -Methode legt die **AudioMapping-Eigenschaft** fest.

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**


</dt> <dd>

Die -Methode legt die **ClipboardMapping-Eigenschaft** fest.

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**


</dt> <dd>

Die -Methode legt die **COMPortMapping-Eigenschaft** fest.

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**


</dt> <dd>

Die -Methode legt die **DriveMapping-Eigenschaft** fest.

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**


</dt> <dd>

Die -Methode legt die **LPTPortMapping-Eigenschaft** fest.

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**


</dt> <dd>

Die -Methode legt die **PNPRedirection-Eigenschaft** fest.

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**


</dt> <dd>

Die -Methode legt die **WindowsPrinterMapping-Eigenschaft** fest.

</dd> </dl> </dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Ein Wert, der angibt, ob die vom *PropertyName-Parameter* angegebene Eigenschaft aktiviert oder deaktiviert werden soll.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deaktivieren Sie die -Eigenschaft.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktivieren Sie die -Eigenschaft.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die angegebene Clienteigenschaft nicht der Gruppenrichtliniensteuerung unterliegt oder wenn die Eigenschafteneinstellung nicht für die Außerkraftsetzung durch den Server geeignet ist.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 


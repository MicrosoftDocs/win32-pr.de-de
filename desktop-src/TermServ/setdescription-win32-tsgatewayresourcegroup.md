---
title: SetDescription-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Legt die Description-Eigenschaft für die Ressourcengruppe fest.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- SetDescription-Methode Remotedesktopdienste
- SetDescription-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, setDescription-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346533"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a>SetDescription-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"

Legt die **Description** -Eigenschaft für die Ressourcengruppe fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Beschreibung* \[ in\]
</dt> <dd>

Beschreibung der Ressourcengruppe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei " \_ zgatewayresourcegroup"**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


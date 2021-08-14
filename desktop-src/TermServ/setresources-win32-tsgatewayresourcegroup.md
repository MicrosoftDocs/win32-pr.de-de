---
title: SetResources-Methode der Win32_TSGatewayResourceGroup Klasse
description: Legt die Resources-Eigenschaft für diese Ressourcengruppe fest.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- SetResources-Remotedesktopdienste
- SetResources-Methode Remotedesktopdienste , Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup klasse Remotedesktopdienste , SetResources-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f357b08e554c5fa97cc26d15c52e65a0668512eeef20bceeba8d194510bdf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987670"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>SetResources-Methode der Win32 \_ TSGatewayResourceGroup-Klasse

Legt die **Resources-Eigenschaft** für diese Ressourcengruppe fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ressourcen* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste der Ressourcen in dieser Ressourcengruppe. Ein \* "" steht für alle Ressourcen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Wenn sich mehrere Ressourcen im *Resources-Parameter* befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


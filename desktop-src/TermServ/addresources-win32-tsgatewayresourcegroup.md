---
title: AddResources-Methode der Win32_TSGatewayResourceGroup Klasse
description: Fügt der Ressourcengruppe Ressourcen hinzu.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- AddResources-Remotedesktopdienste
- AddResources-Methode Remotedesktopdienste , Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup klasse Remotedesktopdienste , AddResources-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c51e42a8d279823e0b56e97aa85987dc919ee788497f464d62e25b8e0f18199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757876"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>AddResources-Methode der Win32 \_ TSGatewayResourceGroup-Klasse

Fügt der Ressourcengruppe Ressourcen hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ressourcen* \[ In\]
</dt> <dd>

Durch Semikolons getrennte Liste der Ressourcen, die der Ressourcengruppe hinzugefügt werden sollen. Ein \* "" steht für alle Ressourcen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Wenn sich mehrere Ressourcen im *Resources-Parameter* befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


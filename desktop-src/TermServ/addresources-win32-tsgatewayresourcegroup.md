---
title: Adresssources-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Fügt der Ressourcengruppe Ressourcen hinzu.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Adresssources-Methode Remotedesktopdienste
- Adresssources-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, adresssources-Methode
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
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517462"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Adresssources-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"

Fügt der Ressourcengruppe Ressourcen hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ressourcen* \[ in\]
</dt> <dd>

Durch Semikolons getrennte Liste von Ressourcen, die der Ressourcengruppe hinzugefügt werden sollen. Ein " \* " bedeutet alle Ressourcen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Wenn sich mehrere Ressourcen im *Ressourcen* Parameter befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.

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

 


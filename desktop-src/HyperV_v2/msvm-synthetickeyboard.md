---
description: Stellt ein synthetisches Tastatur Gerät dar.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353023"
---
# <a name="msvm_synthetickeyboard-class"></a>MSVM \_ synthetickeyboard-Klasse

Stellt ein synthetisches Tastatur Gerät dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>Member

Die **MSVM \_ synthetickeyboard** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM \_ synthetickeyboard** -Klasse verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-synthetickeyboard-requeststatechange.md) | Fordert eine Statusänderung an.<br/> |
| [**Zurücksetzen**](msvm-synthetickeyboard-reset.md)                           | setzt das Gerät zurück.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ userdevice**](cim-userdevice.md)
</dt> </dl>

 

 





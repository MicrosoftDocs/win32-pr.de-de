---
description: Vergleichen Sie das Argument mit der aktiven Konfiguration des Collectors.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: IsConfigurationEqual-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 6facd4f885eb1eb992f95bf4432e32704f7472d8125cb1022f7a6baf5cf591d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579670"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>IsConfigurationEqual-Methode der Control-Klasse

Vergleichen Sie das Argument mit der aktiven Konfiguration des Collectors.

## <a name="syntax"></a>Syntax


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Konfiguration* \[ In\]
</dt> <dd>

Die Konfiguration, die mit der aktiven Konfiguration verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>


</dt> <dd>

0

Fehler

</dd> <dt>


</dt> <dd>

1

Erfolg

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 





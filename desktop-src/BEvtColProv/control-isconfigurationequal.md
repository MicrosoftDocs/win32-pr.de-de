---
description: Vergleichen Sie das-Argument mit der aktiven Konfiguration des Sammlers.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Isconfigurationequal-Methode der Control-Klasse
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
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747785"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Isconfigurationequal-Methode der Control-Klasse

Vergleichen Sie das-Argument mit der aktiven Konfiguration des Sammlers.

## <a name="syntax"></a>Syntax


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Config* \[ in\]
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>Booteventcollector WMI. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 





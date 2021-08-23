---
description: Liest die aktive Konfiguration des Collectors.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: GetConfiguration-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: a877b4ae061b6568b877d9b8ee65b8d9b0380a012d7fdba28408ad4bfcae7030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579720"
---
# <a name="getconfiguration-method-of-the-control-class"></a>GetConfiguration-Methode der Control-Klasse

Liest die aktive Konfiguration des Collectors.

## <a name="syntax"></a>Syntax


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TimestampLow* \[ out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die Bits mit niedriger Reihenfolge eines Zeitstempels, der angibt, wann die Konfiguration festgelegt wurde.

</dd> <dt>

*TimestampHigh* \[ out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die hohen Bits eines Zeitstempels, der angibt, wann die Konfiguration festgelegt wurde.

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
| Namespace<br/>                | \\Stamm-Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 





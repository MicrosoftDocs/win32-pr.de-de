---
description: Lesen Sie die aktive Konfiguration des Sammlers.
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
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958160"
---
# <a name="getconfiguration-method-of-the-control-class"></a>GetConfiguration-Methode der Control-Klasse

Lesen Sie die aktive Konfiguration des Sammlers.

## <a name="syntax"></a>Syntax


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TimeStampLow* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die nieder wertigen Bits eines Zeitstempels, der angibt, wann die Konfiguration festgelegt wurde.

</dd> <dt>

*TimeStampHigh* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die höherwertigen Bits eines Zeitstempels, der angibt, wann die Konfiguration festgelegt wurde.

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

 

 





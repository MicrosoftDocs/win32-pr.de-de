---
description: Überprüfen Sie einen Konfigurations Text auf Richtigkeit, ohne ihn als aktiv festzulegen. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Validateconfiguration-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958157"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Validateconfiguration-Methode der Control-Klasse

Überprüfen Sie einen Konfigurations Text auf Richtigkeit, ohne ihn als aktiv festzulegen. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.

## <a name="syntax"></a>Syntax


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Config* \[ in\]
</dt> <dd>

Die Konfiguration, die überprüft werden soll.

</dd> <dt>

*ErrorString* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter eine Beschreibung des Validierungs Fehlers für den Vorgang, wenn ein Fehler aufgetreten ist.

</dd> <dt>

*Warningstring* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter eine Beschreibung aller Validierungs Warnungen für den Vorgang.

Die Text Zeichenfolge mit Warnungen.

</dd> <dt>

*InfoString* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter einen Satz von Informationen zur Konfiguration.

</dd> <dt>

*ErrorType* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, gibt dieser Parameter den Fehlertyp an, wenn ein Validierungs Fehler aufgetreten ist.

Mögliche Werte sind:

<dt>

0
</dt> <dd>

Das Argument fehlt.

</dd> <dt>

1
</dt> <dd>

Das Argument Format ist ungültig.

</dd> <dt>

2
</dt> <dd>

Ein Konfigurations Argument ist ungültig.

</dd> </dl> </dd> </dl>

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

 

 





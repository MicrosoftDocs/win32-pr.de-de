---
description: Legen Sie die neue aktive Konfiguration des Collectors fest.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: SetConfiguration-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 41ff2c97eaa4b3e2080493c640b716ae4a822762b0f598c94e141a8cc4b4ac6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589070"
---
# <a name="setconfiguration-method-of-the-control-class"></a>SetConfiguration-Methode der Control-Klasse

Legen Sie die neue aktive Konfiguration des Collectors fest.

## <a name="syntax"></a>Syntax


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Konfiguration* \[ In\]
</dt> <dd>

Die zu aktivierende Konfiguration.

</dd> <dt>

*OldTimestampLow* \[ In\]
</dt> <dd>

Die niedrigen Bits eines Zeitstempels, der angibt, wann die aktuelle aktive Konfiguration festgelegt wurde. Die Atomaritätsprüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*OldTimestampHigh* \[ In\]
</dt> <dd>

Die hohen Bits eines Zeitstempels, der angibt, wann die aktuelle aktive Konfiguration festgelegt wurde. Die Atomaritätsprüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die niedrigen Bits eines Zeitstempels, der angibt, wann die neue Konfiguration festgelegt wurde. Die Atomaritätsprüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die hohen Bits des Zeitstempels, der angibt, wann die neue Konfiguration festgelegt wurde. Die Atomaritätsprüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Wenn diese Methode einen Fehler zurückgibt, enthält dieser Parameter die Fehlerbeschreibung.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter alle Warnmeldungen für den Vorgang.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter Informationen für die neue aktive Konfiguration.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Wenn bei dieser Methode ein Fehler aufgetreten ist, gibt dieser Parameter den Fehlertyp an.

<dt>

0
</dt> <dd>

Die neue Konfiguration fehlt.

</dd> <dt>

1
</dt> <dd>

Das Format der neuen Konfiguration ist ungültig.

</dd> <dt>

2
</dt> <dd>

Die neue Konfiguration ist ungültig.

</dd> <dt>

3
</dt> <dd>

Es ist ein Fehler aufgetreten, der durch einen geöffneten Socket verursacht wurde.

</dd> <dt>

4
</dt> <dd>

Es ist ein Datei-Schreibfehler aufgetreten.

</dd> <dt>

5
</dt> <dd>

Es ist ein Atomaritätsfehler aufgetreten.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 





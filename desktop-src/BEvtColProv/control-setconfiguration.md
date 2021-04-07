---
description: Legen Sie die neue aktive Konfiguration des Sammlers fest.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: SetConfiguration-Methode der Steuerelement Klasse
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
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747784"
---
# <a name="setconfiguration-method-of-the-control-class"></a>SetConfiguration-Methode der Steuerelement Klasse

Legen Sie die neue aktive Konfiguration des Sammlers fest.

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

*Config* \[ in\]
</dt> <dd>

Die zu Aktivier-Konfiguration.

</dd> <dt>

*Oldtimestamplow* \[ in\]
</dt> <dd>

Die nieder wertigen Bits eines Zeitstempels, der angibt, wann die aktuelle aktive Konfiguration festgelegt wurde. Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*Oldtimestamphigh* \[ in\]
</dt> <dd>

Die höherwertigen Bits eines Zeitstempels, der angibt, wann die aktuelle aktive Konfiguration festgelegt wurde. Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*Newtimestamplow* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die nieder wertigen Bits eines Zeitstempels, der angibt, wann die neue Konfiguration festgelegt wurde. Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*Newtimestamphigh* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die höherwertigen Bits des Zeitstempels, der angibt, wann die neue Konfiguration festgelegt wurde. Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.

</dd> <dt>

*ErrorString* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die Fehlerbeschreibung, wenn ein Fehler aufgetreten ist.

</dd> <dt>

*Warningstring* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameter alle Warnmeldungen für den Vorgang.

</dd> <dt>

*InfoString* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, enthält dieser Parameterinformationen für die neue aktive Konfiguration.

</dd> <dt>

*ErrorType* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode zurückgegeben wird, gibt dieser Parameter den Fehlertyp an, wenn ein Fehler aufgetreten ist.

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

Fehler beim Schreiben von Dateien.

</dd> <dt>

5
</dt> <dd>

Unteilbarkeit-Fehler.

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

 

 





---
description: Die pdhvbgetdoublecountervalue-Funktion gibt den aktuellen Wert des angegebenen Zählers als Gleit Komma Wert mit doppelter Genauigkeit zurück.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: Pdhvbgetdoublecountervalue-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345509"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>Pdhvbgetdoublecountervalue-Funktion

Die **pdhvbgetdoublecountervalue** -Funktion gibt den aktuellen Wert des angegebenen Zählers als Gleit Komma Wert mit doppelter Genauigkeit zurück. Sie sollten den *Counter-Status* vor der Rückgabe der zurückgegebenen Nummer überprüfen, da der Indikator beim Lesen möglicherweise nicht gültig ist. Zum Überprüfen des Status des Zählers wird die [**pdhvbisgoodstatus**](pdhvbisgoodstatus.md) -Funktion aufgerufen.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion "pdhvbgetdoublecountervalue" ( \_ ByVal counterhandle "Long", \_ ByVal counterstatus "Long" \_ ) als "Double"

## <a name="parameters"></a>Parameter

<dl> <dt>

*Counter handle* 
</dt> <dd>

ID des Zählers, dessen aktueller Wert gelesen werden soll.

</dd> <dt>

*Gegen Status* 
</dt> <dd>

Variable, in der der aktuelle Status des Leistungs Zählers an den Aufrufer zurückgegeben wird. Der zurückgegebene Datenwert ist nur gültig, wenn der im counterstatus zurückgegebene Wert PDH \_ cstatus \_ gültige \_ Daten oder PDH \_ cstatus \_ New \_ Data ist (siehe PDH-Fehlercodes). Wenn der in Counter Status zurückgegebene Wert ein beliebiger anderer Wert ist, verwenden Sie die Daten nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt den Gleit Komma Wert mit doppelter Genauigkeit des aktuellen Zählers zurück, berechnet und formatiert, wie vom Zählertyp definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhvbisgoodstatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 





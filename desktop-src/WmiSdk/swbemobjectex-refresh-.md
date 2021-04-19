---
description: Aktualisiert die Daten für Objekte mit Daten, die von einem Leistungs Anbieter bereitgestellt werden, z. b. die Leistungsdaten. Aktualisierbare Daten können schneller und ohne einen aufzurufenden Austausch von "Swap Services. Get" abgerufen werden \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: SWbemObjectEx.Refresh_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355608"
---
# <a name="swbemobjectexrefresh_-method"></a>Errbemubjectex. Refresh- \_ Methode

Mit **der \_ Refresh** -Methode von " [**errbemubjectex**](swbemobjectex.md) " werden die Daten für Objekte aktualisiert, die von einem Leistungs Anbieter bereitgestellte Daten enthalten, wie z. b. die [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes)Daten. Aktualisierbare Daten können schneller und ohne einen aufzurufenden [**Austausch von " \_ Swap Services. Get**](swbemservices-get.md)" abgerufen werden.

Weitere Informationen zu dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reservierte Vorgangs Flags, die, falls angegeben, 0 (null) sein müssen.

</dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Ein [**-**](swbemnamedvalueset.md) Objekt, das den Kontext für den Vorgang festlegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Aktualisierungs \_** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Der Anbieter ist intern fehlgeschlagen, auch wenn der Vorgang gültig war.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Format wurde nicht gefunden.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Einer der Parameter für den Aufruf ist nicht korrekt.

</dd> <dt>

**wbemErrRefresherBusy** -2147749975 (0x80041057)
</dt> <dd>

Die Aktualisierungsroutine ist mit einer anderen Operation ausgelastet.

</dd> <dt>

**wbempartialresults** -2147745808 (0x80040010)
</dt> <dd>

Nicht alle Objekte, Enumeratoren oder gedugten Aktualisierungs Zeichen wurden erfolgreich aktualisiert. Diese Rückgabe ist kein Fehler, aber ein Hinweis darauf, dass der Vorgang unvollständig war.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Skriptcode Beispiel wird veranschaulicht, wie sowohl Rohdaten als auch gekochte Leistungsindikatoren für den System Prozess abgerufen werden. Die Objekte werden alle zwei Sekunden aktualisiert, und die angezeigten Eigenschaften werden angezeigt.


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch<br/>                                                         |
| IID<br/>                      | IID \_ iswbejebjectex<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austauschen von "errbemubjectex"**](swbemobjectex.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 


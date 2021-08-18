---
description: Aktualisiert die Daten für Objekte mit Daten, die von einem Leistungsanbieter bereitgestellt werden, z. B. leistungsindikatorklassen. Sie können aktualisierte Daten schneller und ohne einen Aufruf von SWbemServices.Get \_ abrufen.
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: SWbemObjectEx.Refresh_-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 6763607d2b5f29d32e722e5a1159a1fc276e546c4af9c2e5da10b1d4b2f08235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991940"
---
# <a name="swbemobjectexrefresh_-method"></a>SWbemObjectEx.Refresh-Methode \_

Die **\_ Refresh-Methode** von [**SWbemObjectEx**](swbemobjectex.md) aktualisiert die Daten für Objekte, deren Daten von einem Leistungsanbieter bereitgestellt werden, z. B. die [Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes). Sie können aktualisierte Daten schneller und ohne einen Aufruf von [**SWbemServices.Get \_**](swbemservices-get.md)abrufen.

Weitere Informationen zu dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reservierte Vorgangsflags, die, falls angegeben, 0 (null) sein müssen.

</dd> <dt>

*objWbemNamedValueSet* \[ in, optional\]
</dt> <dd>

Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das den Kontext für den Vorgang festlegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Refresh-Methode \_** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Der Anbieter ist intern fehlgeschlagen, obwohl der Vorgang gültig war.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Format wurde nicht gefunden.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Einer der Parameter für den Aufruf ist nicht korrekt.

</dd> <dt>

**wbemErrRefresherBusy** – 2147749975 (0x80041057)
</dt> <dd>

Die Aktualisierungsroutine ist mit einer anderen Operation ausgelastet.

</dd> <dt>

**wbemPartialResults** – 2147745808 (0x80040010)
</dt> <dd>

Nicht alle Objekte, Enumeratoren oder geschachtelten Aktualisierungen wurden erfolgreich aktualisiert. Diese Rückgabe ist kein Fehler, sondern ein Hinweis darauf, dass der Vorgang unvollständig war.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Skriptcodebeispiel zeigt, wie Sie sowohl rohe als auch verarbeitete Leistungsindikatoren für den Systemprozess abrufen. Die Objekte werden alle zwei Sekunden aktualisiert, und die Eigenschaften werden angezeigt.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 


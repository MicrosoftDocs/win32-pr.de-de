---
description: Formatiert ein Datum als Datums Zeichenfolge für ein angegebenes Gebiets Schema.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: Getdateformatwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215948"
---
# <a name="getdateformatwrapw-function"></a>Getdateformatwrapw-Funktion

\[**Getdateformatwrapw** ist für die Verwendung in Windows XP verfügbar. Sie wird in nachfolgenden Versionen nicht verfügbar sein. Sie sollten [**getdateformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) an seiner Stelle verwenden.\]

Formatiert ein Datum als Datums Zeichenfolge für ein angegebenes Gebiets Schema. Die-Funktion formatiert entweder ein bestimmtes Datum oder das lokale Systemdatum.

> [!Note]  
> **Getdateformatwrapw** ist ein Wrapper für die **getdateformatw** -Funktion. Weitere Hinweise zur Verwendung finden Sie auf der Seite " [**getDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) ".

 

## <a name="syntax"></a>Syntax


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gebiets Schema  \[ in\]
</dt> <dd>

Typ: **LCID**

Das Gebiets Schema, für das die Datums Zeichenfolge formatiert werden soll. Wenn *pwzformat* den Wert **null** hat, formatiert die Funktion die Zeichenfolge gemäß dem Datumsformat für dieses Gebiets Schema. Wenn *pwzformat* nicht **null** ist, verwendet die Funktion das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind (z. b. die Tages-und Monatsnamen des Gebiets Schemas).

Bei diesem Parameter kann es sich um einen vom [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) -Makro erstellten Gebiets Schema Bezeichner oder einen der folgenden vordefinierten Werte handeln.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**Standard für Gebiets Schema \_ System \_**


</dt> <dd>

Standardsystem Gebiets Schema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Standardbenutzer Name für locale \_**


</dt> <dd>

Standardbenutzer Gebiets Schema.

</dd> </dl> </dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Typ: **DWORD**

Gibt verschiedene Funktions Optionen an. Wenn *pwzformat* nicht **null** ist, muss dieser Parameter NULL sein. Wenn *pwzformat* **null** ist, können Sie eine Kombination der folgenden Werte angeben. Wenn Sie weder Date \_ yearMonth, Date \_ SHORTDATE noch Date \_ longDate angeben und *pwzformat* den Wert **null** hat, \_ wird Date SHORTDATE als Standardwert verwendet.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**Gebiets Schema \_ nouseroverride**


</dt> <dd>

Wenn festgelegt, formatiert die Funktion die Zeichenfolge unter Verwendung des Standard Datums Formats des Systems für das angegebene Gebiets Schema. Wenn nicht festgelegt, formatiert die Funktion die Zeichenfolge mithilfe von Benutzer Überschreibungen für das Standard Datumsformat des Gebiets Schemas.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Gebiets Schema \_ verwenden \_ CP \_ ACP**


</dt> <dd>

Verwendet die ANSI-Codepage des Systems für die Zeichen folgen Übersetzung anstelle der Codepage des Gebiets Schemas.

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Datum/ \_ kurzdatum**


</dt> <dd>

Verwendet das kurze Datumsformat. Dieser Wert kann nicht mit Date \_ longDate oder Date \_ yearMonth verwendet werden.

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Datum \_ longDate**


</dt> <dd>

Verwendet das lange Datumsformat. Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ yearMonth verwendet werden.

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Datum des \_ Monats**


</dt> <dd>

Verwendet das Format Jahr/Monat. Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ longDate verwendet werden.

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**Datum der \_ Verwendung des \_ alt- \_ Kalenders**


</dt> <dd>

Verwendet den alternativen Kalender, falls vorhanden, um die Datums Zeichenfolge zu formatieren. Wenn dieses Flag festgelegt ist, verwendet die Funktion das Standardformat für diesen alternativen Kalender anstelle von Benutzer Überschreibungen. Die Benutzer Überschreibungen werden nur in dem Fall verwendet, dass kein Standardformat für den angegebenen alternativen Kalender vorhanden ist.

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Datums- \_ ltrreading**


</dt> <dd>

Fügt Markierungen für das Lese Layout von links nach rechts hinzu. Dieser Wert kann nicht mit Date \_ RtlReading verwendet werden.

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Datum \_ RtlReading**


</dt> <dd>

Fügt Markierungen für das Lese Layout von rechts nach Links hinzu. Dieser Wert kann nicht mit dem Datum \_ ltrreading verwendet werden.

</dd> </dl> </dd> <dt>

*lpdate* \[ in\]
</dt> <dd>

Typ: * Konstante *[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Ein Zeiger auf eine [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Datumsinformationen enthält, die formatiert werden sollen. Wenn dieser Zeiger **null** ist, verwendet die Funktion das aktuelle lokale Systemdatum.

</dd> <dt>

*pwzformat* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf ein Format Bild, das zum bilden der Datums Zeichenfolge verwendet werden soll. Wenn *pwzformat* den Wert **null** hat, verwendet die Funktion das Datumsformat des angegebenen Gebiets Schemas. Weitere Informationen finden Sie unter " [**getDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) ".

</dd> <dt>

*pwzdatestr* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR**

Ein Zeiger auf einen Puffer, der die formatierte Datums Zeichenfolge empfängt.

</dd> <dt>

*cchdate* \[ in\]
</dt> <dd>

Typ: **int**

Gibt die Größe des *pwzdatestr* -Puffers in Zeichen an. Wenn *cchdate* NULL ist, gibt die Funktion die Anzahl von Zeichen zurück, die für die formatierte Datums Zeichenfolge erforderlich ist, und der Puffer, auf den *pwzdatestr* zeigt, wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Anzahl der Zeichen, die in den Puffer geschrieben werden, auf den *pwzdatestr* zeigt. Wenn der *cchdate* -Parameter 0 (null) ist, ist der Rückgabewert die Anzahl von Zeichen, die für die formatierte Datums Zeichenfolge erforderlich ist. Die Anzahl schließt das abschließende Null Zeichen ein.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf. " **GetLastError** " kann einen der folgenden Fehlercodes zurückgeben.

<dl> <dt>

**Fehler \_ beim \_ Puffer.**
</dt> <dt>

**\_ungültige \_ Flags.**
</dt> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Getdateformatwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen als Windows XP zu verwenden. Die bevorzugte Methode ist die Verwendung von [**getdateformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Getdateformatwrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe von Ordnungszahl 311.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 

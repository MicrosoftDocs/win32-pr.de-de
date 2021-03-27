---
description: Formatiert die Zeit als Zeit Zeichenfolge für ein bestimmtes Gebiets Schema.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: Gettimeformatwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979648"
---
# <a name="gettimeformatwrapw-function"></a>Gettimeformatwrapw-Funktion

\[**Gettimeformatwrapw** ist für die Verwendung in Windows XP verfügbar. Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar. Sie sollten [**gettimeformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) an seiner Stelle verwenden.\]

Formatiert die Zeit als Zeit Zeichenfolge für ein bestimmtes Gebiets Schema. Die-Funktion formatiert entweder eine angegebene Zeit oder eine lokale Systemzeit.

> [!Note]  
> **Gettimeformatwrapw** ist ein Wrapper für die **gettimeformatw** -Funktion. Weitere Hinweise zur Verwendung finden Sie auf der Seite [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

 

## <a name="syntax"></a>Syntax


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gebiets Schema  \[ in\]
</dt> <dd>

Typ: **LCID**

Gibt das Gebiets Schema an, für das die Zeit Zeichenfolge formatiert werden soll. Wenn *pwzformat* den Wert **null** hat, formatiert die Funktion die Zeichenfolge gemäß dem Zeitformat für dieses Gebiets Schema. Wenn *pwzformat* nicht **null** ist, verwendet die Funktion das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind (z. b. die Zeit Marker des Gebiets Schemas).

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

Gibt verschiedene Funktions Optionen an. Sie können eine Kombination der folgenden Werte angeben.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**Gebiets Schema \_ nouseroverride**


</dt> <dd>

Wenn festgelegt, formatiert die Funktion die Zeichenfolge mit dem System Standard-Zeitformat für das angegebene Gebiets Schema. Wenn nicht festgelegt, formatiert die Funktion die Zeichenfolge mithilfe von Benutzer Überschreibungen für das Standardzeit Format des Gebiets Schemas. Dieses Flag kann nur festgelegt werden, wenn *pwzformat* **null** ist.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Gebiets Schema \_ verwenden \_ CP \_ ACP**


</dt> <dd>

Verwendet die ANSI-Codepage des Systems für die Zeichen folgen Übersetzung anstelle der Gebiets Schema-Codepage.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**Zeit ( \_ nominutesorseconds)**


</dt> <dd>

Verwendet keine Minuten oder Sekunden.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**Zeit (in \_ Sekunden)**


</dt> <dd>

Verwendet keine Sekunden.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**Zeit \_ notimemarker**


</dt> <dd>

Verwendet keinen Zeit Marker.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**Zeit \_ FORCE24HOURFORMAT**


</dt> <dd>

Verwendet immer ein 24-Stunden-Zeitformat.

</dd> </dl> </dd> <dt>

*lptime* \[ in\]
</dt> <dd>

Typ: * Konstante *[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Ein Zeiger auf eine [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die zu formatierenden Zeit Informationen enthält. Wenn dieser Zeiger **null** ist, verwendet die Funktion die aktuelle lokale Systemzeit.

</dd> <dt>

*pwzformat* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf ein Format, das zum bilden der Zeit Zeichenfolge verwendet werden soll. Wenn *pwzformat* den Wert **null** hat, verwendet die Funktion das Zeitformat des angegebenen Gebiets Schemas. Weitere Informationen finden Sie unter [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

</dd> <dt>

*pwztimestr* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR**

Ein Zeiger auf einen Puffer, der die formatierte Zeit Zeichenfolge empfängt.

</dd> <dt>

*cchtime* \[ in\]
</dt> <dd>

Typ: **int**

Die Größe des *pwztimestr* -Puffers in Zeichen. Wenn *cchtime* NULL ist, gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Zeit Zeichenfolge erforderlich sind, und der Puffer, auf den *pwztimestr* zeigt, wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Anzahl der Zeichen, die in den Puffer geschrieben werden, auf den *pwztimestr* zeigt. Wenn der *cchtime* -Parameter 0 (null) ist, ist der Rückgabewert die Anzahl von Zeichen, die für die formatierte Zeit Zeichenfolge erforderlich ist. Die Anzahl schließt das abschließende Null Zeichen ein.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf. " **GetLastError** " kann einen der folgenden Fehlercodes zurückgeben.

<dl> <dt>

**Fehler \_ beim \_ Puffer.**
</dt> <dt>

**\_ungültige \_ Flags.**
</dt> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Gettimeformatwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen als Windows XP zu verwenden. Die bevorzugte Methode ist die Verwendung von [**gettimeformatw**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Gettimeformatwrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe von Ordnungszahl 310.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 

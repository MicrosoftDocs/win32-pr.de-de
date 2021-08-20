---
description: Veraltet.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: db6bf4fc20c24e91a0af29dc8ee81f7a77ef5cb1c0f0e0f6c5a0a792e52eb903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068220"
---
# <a name="getcalendardateformatex-function"></a>GetCalendarDateFormatEx-Funktion

Veraltet. Ruft eine ordnungsgemäß formatierte Datumszeichenfolge für das angegebene Locale unter Verwendung des angegebenen Datums und Kalenders ab. Der Benutzer kann das kurze Datumsformat, das lange Datumsformat, das Jahresmonatsformat oder ein benutzerdefiniertes Formatmuster angeben.

> [!Note]  
> Diese Funktion kann Daten abrufen, die sich zwischen Releases ändern, z. B. aufgrund eines benutzerdefinierten Locale. Wenn Ihre Anwendung Daten beibehalten oder übertragen muss, finden Sie weitere Informationen unter [Verwenden von persistenten Locale Data.](using-persistent-locale-data.md)

 

## <a name="syntax"></a>Syntax


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszLocale* \[ In\]
</dt> <dd>

Zeiger auf einen Locale-Namen oder einen der folgenden vordefinierten Werte.

-   [LOCALE \_ NAME \_ INVARIANT](locale-name-constants.md)
-   [LOCALE \_ NAME \_ SYSTEM \_ DEFAULT](locale-name-constants.md)
-   [LOCALE \_ NAME \_ USER \_ DEFAULT](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die Datumsformatoptionen angeben. Wenn *lpFormat* nicht auf **NULL festgelegt ist,** muss dieser Parameter auf 0 festgelegt werden. Wenn *lpFormat* auf **NULL festgelegt ist,** kann die Anwendung eine Kombination der folgenden Werte und [LOCALE \_ NOUSEROVERRIDE angeben.](locale-nouseroverride.md)



| Wert                                                                                                                                                               | Bedeutung                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**DATE \_ SHORTDATE**</dt> </dl>    | Verwenden Sie das kurze Datumsformat. Dies ist die Standardoption. Dieser Wert kann nicht mit DATE \_ LONGDATE oder DATE \_ YEARMONTH verwendet werden. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**DATE \_ LONGDATE**</dt> </dl>       | Verwenden Sie das lange Datumsformat. Dieser Wert kann nicht mit DATE \_ SHORTDATE oder DATE \_ YEARMONTH verwendet werden. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**DATE \_ YEARMONTH**</dt> </dl>    | Verwenden Sie das Jahres-/Monatsformat. Dieser Wert kann nicht mit DATE \_ SHORTDATE oder DATE \_ LONGDATE verwendet werden.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**DATE \_ LTRREADING**</dt> </dl> | Fügen Sie Markierungen für das Leselayout von links nach rechts hinzu. Dieser Wert kann nicht mit DATE \_ RTLREADING verwendet werden.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**DATE \_ RTLREADING**</dt> </dl> | Fügen Sie Markierungen für das Leselayout von rechts nach links hinzu. Dieser Wert kann nicht mit DATE \_ LTRREADING verwendet werden.<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ In\]
</dt> <dd>

Zeiger auf eine [**CALDATETIME-Struktur,**](caldatetime.md) die die zu formatierten Datums- und Kalenderinformationen enthält.

</dd> <dt>

*lpFormat* \[ In\]
</dt> <dd>

Zeiger auf eine Formatbildzeichenfolge, die zum Bilden der Datumszeichenfolge verwendet wird. Mögliche Werte für die Formatbildzeichenfolge sind in Den Bildern im [Format Tag, Monat, Jahr und Zeit definiert.](day--month--year--and-era-format-pictures.md)

Die Formatbildzeichenfolge muss null-terminiert sein. Die Funktion verwendet das -Locale nur für Informationen, die nicht in der Formatbildzeichenfolge angegeben sind, z. B. die Tag- und Monatsnamen für das Locale. Die Anwendung legt diesen Parameter auf **NULL fest,** wenn die Funktion das Datumsformat des angegebenen Locales verwenden soll.

</dd> <dt>

*lpDateStr* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion die formatierte Datumszeichenfolge empfängt.

</dd> <dt>

*cchDate* \[ In\]
</dt> <dd>

Größe des *lpDateStr-Puffers* in Zeichen. Alternativ kann die Anwendung diesen Parameter auf 0 festlegen. In diesem Fall gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Datumszeichenfolge erforderlich sind, und der *lpDateStr-Parameter* wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen zurück, die bei Erfolg in den *lpDateStr-Puffer* geschrieben wurden. Wenn der *cchDate-Parameter* auf 0 festgelegt ist, gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Datumszeichenfolge erforderlich sind, einschließlich des beendenden NULL-Zeichens.

Diese Funktion gibt 0 zurück, wenn sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen zu erhalten, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLERDATUM \_ \_ LIEGT NICHT IM \_ \_ BEREICH. Das angegebene Datum lag nicht im Bereich.
-   FEHLER: \_ NICHT \_ GENÜGEND PUFFER. Eine angegebene Puffergröße war nicht groß genug, oder sie wurde fälschlicherweise auf **NULL festgelegt.**
-   FEHLER \_ \_ UNGÜLTIGE FLAGS. Die für Flags angegebenen Werte waren ungültig.
-   FEHLER \_ \_ UNGÜLTIGER PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Das früheste datum, das von dieser Funktion unterstützt wird, ist der 1. Januar 1601.

Dieser Funktion ist keine Headerdatei oder Bibliotheksdatei zugeordnet. Die Anwendung kann [**LoadLibrary mit**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) dem DLL-Namen (Kernel32.dll) aufrufen, um ein Modulhand handle zu erhalten. Sie kann dann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modulhandle und dem Namen dieser Funktion aufrufen, um die Funktionsadresse zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützung der Landessprache](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Bilder im Format "Tag", "Monat", "Jahr" und "Zeit"](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: Beispiel für namensbasierte APIs](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 

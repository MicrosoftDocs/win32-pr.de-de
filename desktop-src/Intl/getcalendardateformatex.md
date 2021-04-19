---
description: Veraltet.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: Getcalendardateformatex-Funktion
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
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356192"
---
# <a name="getcalendardateformatex-function"></a>Getcalendardateformatex-Funktion

Veraltet. Ruft mit dem angegebenen Datum und Kalender eine ordnungsgemäß formatierte Datums Zeichenfolge für das angegebene Gebiets Schema ab. Der Benutzer kann das kurze Datumsformat, das lange Datumsformat, das Format des Jahres Monats oder ein benutzerdefiniertes Format Muster angeben.

> [!Note]  
> Diese Funktion kann z. b. aufgrund eines benutzerdefinierten Gebiets Schemas Daten abrufen, die sich zwischen Releases ändern. Wenn Ihre Anwendung Daten beibehalten oder übertragen muss, finden Sie weitere Informationen unter [Verwenden von permanenten](using-persistent-locale-data.md)Gebiets Schema Daten.

 

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

*lpszlocale* \[ in\]
</dt> <dd>

Zeiger auf einen Gebiets Schema Namen oder einen der folgenden vordefinierten Werte.

-   [Gebiets Schema \_ Name \_ invariant](locale-name-constants.md)
-   [Standardwert des Gebiets Schema \_ namens \_ Systems \_](locale-name-constants.md)
-   [\_Standard Name \_ des Gebiets Schemas \_](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flags, die Datumsformat Optionen angeben. Wenn *lpformat* nicht auf **null** festgelegt ist, muss dieser Parameter auf 0 festgelegt werden. Wenn *lpformat* auf **null** festgelegt ist, kann die Anwendung eine Kombination der folgenden Werte und [locale \_ nouseroverride](locale-nouseroverride.md)angeben.



| Wert                                                                                                                                                               | Bedeutung                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**Datum/ \_ kurzdatum**</dt> </dl>    | Verwenden Sie das kurze Datumsformat. Dies ist die Standardoption. Dieser Wert kann nicht mit Date \_ longDate oder Date \_ yearMonth verwendet werden. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**Datum \_ longDate**</dt> </dl>       | Verwenden Sie das lange Datumsformat. Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ yearMonth verwendet werden. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**Datum des \_ Monats**</dt> </dl>    | Verwenden Sie das Format Jahr/Monat. Dieser Wert kann nicht mit Date \_ SHORTDATE oder Date \_ longDate verwendet werden.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**Datums- \_ ltrreading**</dt> </dl> | Fügen Sie Markierungen für das Lese Layout von links nach rechts hinzu. Dieser Wert kann nicht mit Date \_ RtlReading verwendet werden.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**Datum \_ RtlReading**</dt> </dl> | Fügen Sie Markierungen für das Lese Layout von rechts nach Links hinzu. Dieser Wert kann nicht mit dem Datum \_ ltrreading verwendet werden.<br/>                        |



 

</dd> <dt>

*lpcaldatetime* \[ in\]
</dt> <dd>

Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die die Datums-und Kalenderinformationen enthält, die formatiert werden sollen.

</dd> <dt>

*lpformat* \[ in\]
</dt> <dd>

Zeiger auf eine Format Bild Zeichenfolge, die verwendet wird, um die Datums Zeichenfolge zu bilden. Mögliche Werte für die Format Bild Zeichenfolge werden im [Format "Tag", "Month", "Year" und "ERA](day--month--year--and-era-format-pictures.md)" definiert.

Die Format Bild Zeichenfolge muss auf Null enden. Die-Funktion verwendet das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind, z. b. die Namen des Tags und Monats für das Gebiets Schema. Die Anwendung legt diesen Parameter auf **null** fest, wenn die Funktion das Datumsformat des angegebenen Gebiets Schemas verwenden soll.

</dd> <dt>

*lpdatestr* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion die formatierte Datums Zeichenfolge empfängt.

</dd> <dt>

*cchdate* \[ in\]
</dt> <dd>

Größe des *lpdatestr* -Puffers in Zeichen. Alternativ kann die Anwendung diesen Parameter auf 0 festlegen. In diesem Fall gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Datums Zeichenfolge erforderlich sind, und der *lpdatestr* -Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen zurück, die bei erfolgreicher Ausführung in den *lpdatestr* -Puffer geschrieben wurden. Wenn der *cchdate* -Parameter auf 0 festgelegt ist, gibt die Funktion die Anzahl der Zeichen zurück, die zum Speichern der formatierten Datums Zeichenfolge erforderlich sind, einschließlich des abschließenden NULL-Zeichens.

Diese Funktion gibt 0 (null) zurück, wenn Sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs. Das angegebene Datum lag außerhalb des gültigen Bereichs.
-   Fehler \_ beim \_ Puffer. Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.
-   \_ungültige \_ Flags. Die für Flags angegebenen Werte waren ungültig.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Das früheste von dieser Funktion unterstützte Datum ist der 1. Januar 1601.

Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei. Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten. Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> <dt>

[Format Abbildungen für Tag, Monat, Jahr und ERA](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: Beispiel für namensbasierte APIs](nls--name-based-apis-sample.md)
</dt> <dt>

[**Enumdateformatsexex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**Caldatetime**](caldatetime.md)
</dt> </dl>

 

 

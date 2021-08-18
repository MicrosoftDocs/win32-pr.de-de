---
description: Stellt eine Liste von Skripts für das angegebene Locale zur Verfügung.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: DownlevelGetLocaleScripts-Funktion (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 02631a605f67f3c27dfcc29c1e660ca24e56b6072d4490ba8ba090ebdd8b9019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068250"
---
# <a name="downlevelgetlocalescripts-function"></a>DownlevelGetLocaleScripts-Funktion

Stellt eine Liste von Skripts für das angegebene Locale zur Verfügung.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCType* aufrufen, der [auf LOCALE \_ SSCRIPTS festgelegt ist.](locale-sscripts.md)

 

## <a name="syntax"></a>Syntax


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpLocaleName* \[ In\]
</dt> <dd>

Zeiger auf einen [Null-Terminierungs-Locale-Namen](locale-names.md).

</dd> <dt>

*lpScripts* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion eine mit NULL beendete Zeichenfolge abruft, die eine Liste von Skripts darstellt, unter Verwendung der 4-Zeichen-Notation, die in [ISO 15924 verwendet wird.](https://www.unicode.org/iso15924/iso15924-codes.html) Jeder Skriptname besteht aus vier lateinischen Zeichen, und die Namen werden in alphabetischer Reihenfolge abgerufen. Jedem davon, einschließlich des letzten, folgt ein Semikolon.

Alternativ kann dieser Parameter NULL **enthalten,** wenn *cchScripts* auf 0 festgelegt ist. In diesem Fall gibt die Funktion die erforderliche Größe für den Skriptpuffer zurück.

</dd> <dt>

*cchScripts* \[ In\]
</dt> <dd>

Größe (in Zeichen) für den Skriptpuffer, der durch *lpScripts angegeben wird.*

Alternativ kann die Anwendung diesen Parameter auf 0 festlegen. In diesem Fall ruft die Funktion **NULL** in *lpScripts* ab und gibt die erforderliche Größe für den Skriptpuffer zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der im Skriptpuffer abgerufenen Zeichen zurück, einschließlich des beendenden NULL-Zeichens. Wenn die Funktion erfolgreich ist und der Wert von *cchScripts* 0 ist, ist der Rückgabewert die erforderliche Größe für den Skriptpuffer in Zeichen, einschließlich eines beendenden NULL-Zeichens.

Diese Funktion gibt 0 zurück, wenn sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen zu erhalten, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER \_ BADDB. Die Funktion konnte nicht auf die Daten zugreifen. Diese Situation sollte normalerweise nicht auftreten und in der Regel auf eine fehlerhafte Installation, ein Datenträgerproblem oder deren Probleme hindeutet.
-   FEHLER: \_ NICHT \_ GENÜGEND PUFFER. Eine angegebene Puffergröße war nicht groß genug, oder sie wurde fälschlicherweise auf **NULL festgelegt.**
-   FEHLER \_ \_ UNGÜLTIGER PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Diese Funktion ist im Rahmen einer Strategie zur Entschärfung von Sicherheitsproblemen im Zusammenhang mit internationalisierten Domänennamen [(IDNs) nützlich.](handling-internationalized-domain-names--idns.md)

Im Folgenden finden Sie einige Beispiele für Eingaben und Ausgaben für diese Funktion, vorausgesetzt, es ist eine ausreichende Puffergröße vorhanden:



| Gebietsschema                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Englisch (USA) | de-DE          | Latn;           |
| Hindi (Indien)           | hi-IN          | Deva;           |
| Japanisch (Japan)        | ja-JP          | Hani; Hira; Kana; |



 

Die Liste enthält nicht das lateinische Skript, es sei denn, es ist ein wesentlicher Bestandteil des Schreibsystems, das für ein Locale verwendet wird. Lateinische Zeichen werden jedoch häufig im Kontext von Locales verwendet, für die sie nicht nativ sind, z. B. für einen fremden Geschäftsnamen. Im obigen Beispiel für Hindi in Indien ist das einzige abgerufene Skript "Deva" (für Devana sollen), obwohl lateinische Zeichen auch im Hindi-Text enthalten sein können. Die [**DownlevelVerifyScripts-Funktion**](downlevelverifyscripts.md) verfügt über ein spezielles Flag, um diesen Fall zu adressieren.

Die erforderliche Headerdatei und DLL sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN)-Entschärfungs-APIs",](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) der im [MSDN Download Center verfügbar ist.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                        |
| Verteilbare Komponente<br/>          | Entschärfungs-APIs von Microsoft Internationalized Domain Name (IDN) unter Windows XP (SP2 oder höher), Windows Server 2003 (SP1 oder höher) oder Windows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützung der Landessprache](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Behandeln von internationalisierten Domänennamen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

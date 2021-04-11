---
description: Stellt eine Liste von Skripts für das angegebene Gebiets Schema bereit.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Downlevelgetlocalescripts-Funktion (idndl. h)
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
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217806"
---
# <a name="downlevelgetlocalescripts-function"></a>Downlevelgetlocalescripts-Funktion

Stellt eine Liste von Skripts für das angegebene Gebiets Schema bereit.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung von erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCTYPE* aufrufen, der auf [locale \_ sscripts](locale-sscripts.md)festgelegt ist.

 

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

*lplocalename* \[ in\]
</dt> <dd>

Zeiger auf einen mit NULL endenden Gebiets Schema [Namen](locale-names.md).

</dd> <dt>

*lpscripts* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion eine auf NULL endende Zeichenfolge abruft, die eine Liste von Skripts mit der in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)verwendeten 4-Zeichen-Notation darstellt. Jeder Skript Name besteht aus vier lateinischen Zeichen, und die Namen werden in alphabetischer Reihenfolge abgerufen. Auf jede dieser, einschließlich der letzten, folgt ein Semikolon.

Alternativ kann dieser Parameter **null** enthalten, wenn *cchscripts* auf 0 festgelegt ist. In diesem Fall gibt die-Funktion die erforderliche Größe für den Skript Puffer zurück.

</dd> <dt>

*cchscripts* \[ in\]
</dt> <dd>

Größe in Zeichen für den Skript Puffer, der von *lpscripts* angegeben wird.

Alternativ kann die Anwendung diesen Parameter auf 0 festlegen. In diesem Fall ruft die Funktion **null** in *lpscripts* ab und gibt die erforderliche Größe für den Skript Puffer zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Zeichen zurück, die im Skript Puffer abgerufen wurden, einschließlich des abschließenden NULL-Zeichens. Wenn die Funktion erfolgreich ist und der Wert von *cchscripts* 0 ist, ist der Rückgabewert die erforderliche Größe (in Zeichen einschließlich eines abschließenden NULL-Zeichens) für den Skript Puffer.

Diese Funktion gibt 0 (null) zurück, wenn Sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ baddb. Die Funktion konnte nicht auf die Daten zugreifen. Diese Situation sollte normalerweise nicht eintreten, und weist in der Regel auf eine fehlerhafte Installation, ein Datenträger Problem oder das like hin.
-   Fehler \_ beim \_ Puffer. Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist als Teil einer Strategie zum mindern von Sicherheitsproblemen im Zusammenhang mit [internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)nützlich.

Im folgenden finden Sie einige Beispiele für Eingaben und Ausgaben für diese Funktion mit einer ausreichenden Puffergröße:



| Gebietsschema                  | *lplocalename* | *lpscripts*     |
|-------------------------|----------------|-----------------|
| Englisch (USA) | de-DE          | Latn           |
| Hindi (Indien)           | hi-IN          | Vas           |
| Japanisch (Japan)        | ja-JP          | Han Hira; Betrieben |



 

Die Liste enthält nicht das lateinische Skript, es sei denn, es ist ein wesentlicher Bestandteil des Schreibsystems, das für ein Gebiets Schema verwendet wird. Lateinische Zeichen werden jedoch häufig im Kontext von Gebiets Schemas verwendet, für die Sie nicht nativ sind, wie bei einem fremden Geschäftsnamen. Im obigen Beispiel für Hindi in Indien ist das einzige abgerufene Skript "Deva" (für "Devanagari"), obwohl auch lateinische Zeichen in Hindi-Text vorkommen können. Die [**downlevelverifyscripts**](downlevelverifyscripts.md) -Funktion verfügt über ein spezielles Flag, um diesen Fall zu beheben.

Die erforderliche Header Datei und dll sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , der im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                        |
| Verteilbare Komponente<br/>          | Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs unter Windows XP (SP2 oder höher), Windows Server 2003 (SP1 oder höher) oder Windows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> <dt>

[Umgang mit internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**Downlevelgetstringscripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**Downlevelverifyscripts**](downlevelverifyscripts.md)
</dt> <dt>

[**Getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

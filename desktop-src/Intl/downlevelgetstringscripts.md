---
description: Stellt eine Liste der Skripts zur Verfügung, die in der angegebenen Unicode-Zeichenfolge verwendet werden.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: DownlevelGetStringScripts-Funktion (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 23eca82d97ac1da2d0f179c6e670ed032a57410490dcc5a52cf3005d75d65b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041620"
---
# <a name="downlevelgetstringscripts-function"></a>DownlevelGetStringScripts-Funktion

Stellt eine Liste der Skripts zur Verfügung, die in der angegebenen Unicode-Zeichenfolge verwendet werden.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetStringScripts aufrufen.**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)

 

## <a name="syntax"></a>Syntax


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die Optionen für den Skriptabruf angeben.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ ALLOW \_ INHERITED \_ COMMON**</dt> </dl> | Abrufen der Skriptinformationen "Qaii" (INHERITED) und "Zyyy" (COMMON). Dieser Wert wirkt sich nicht auf die Verarbeitung nicht zugewiesener Zeichen aus. Diese Zeichen in der Eingabezeichenfolge bewirken immer, dass ein "Zzzz" (UNASSIGNED-Skript) in der Skriptzeichenfolge angezeigt wird.<br/> |



 

> [!Note]  
> Standardmäßig ignoriert diese Funktion alle geerbten oder allgemeinen Zeichen in der Eingabe-Unicode-Zeichenfolge. Wenn GSS ALLOW INHERITED COMMON nicht festgelegt ist, werden \_ \_ weder "Qaii" noch "Zyyy" in der Skriptzeichenfolge angezeigt, auch wenn die Eingabezeichenfolge solche Zeichen \_ enthält. Wenn GSS ALLOW INHERITED COMMON festgelegt ist und die Eingabezeichenfolge geerbte und/oder allgemeine Zeichen enthält, werden \_ \_ \_ "Qaii" und/oder "Zyyy" in der Skriptzeichenfolge angezeigt. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

 

</dd> <dt>

*lpString* \[ In\]
</dt> <dd>

Zeiger auf die zu analysierende Unicode-Zeichenfolge.

</dd> <dt>

*cchString* \[ In\]
</dt> <dd>

Größe der durch *lpString* angegebenen Unicode-Zeichenfolge in Zeichen. Die Anwendung legt diesen Parameter auf -1 fest, wenn die Zeichenfolge null-terminiert ist. Wenn die Anwendung diesen Parameter auf 0 setzt, ruft die Funktion eine UNICODE-NULL-Zeichenfolge (L" \\ 0") in *lpScripts* ab und gibt 1 zurück.

</dd> <dt>

*lpScripts* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion eine mit NULL beendete Zeichenfolge abruft, die eine Liste von Skripts darstellt, unter Verwendung der 4-Zeichen-Notation, die in [ISO 15924 verwendet wird.](https://www.unicode.org/iso15924/iso15924-codes.html) Jeder Skriptname besteht aus vier lateinischen Zeichen, und die Namen werden in alphabetischer Reihenfolge abgerufen. Auf jeden Namen, einschließlich des letzten, folgt ein Semikolon.

Alternativ kann dieser Parameter NULL **enthalten,** wenn *cchScripts auf* 0 festgelegt ist. In diesem Fall gibt die Funktion die erforderliche Größe für den Skriptpuffer zurück.

</dd> <dt>

*cchScripts* \[ In\]
</dt> <dd>

Größe (in Zeichen) für den Skriptpuffer, der durch *lpScripts angegeben wird.*

Alternativ kann die Anwendung diesen Parameter auf 0 festlegen. In diesem Fall ruft die Funktion **NULL** in *lpScripts* ab und gibt die erforderliche Größe für den Skriptpuffer zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der im Ausgabepuffer abgerufenen Zeichen zurück, einschließlich eines beendenden NULL-Zeichens, sofern erfolgreich, und *cchScripts* wird auf einen Wert ungleich 0 (null) festgelegt. Die Funktion gibt 1 zurück, um anzugeben, dass kein Skript gefunden wurde, z. B. wenn die Eingabezeichenfolge nur COMMON- oder INHERITED-Zeichen enthält und GSS ALLOW INHERITED COMMON nicht \_ \_ festgelegt \_ ist. Da jedes gefundene Skript fünf Zeichen (vier Zeichen + Trennzeichen) hinzufügt, stellt eine einfache mathematische Operation die Skriptanzahl als (Rückgabecode \_ - 1) / 5.

Wenn die Funktion erfolgreich ist und der Wert von *cchScripts* 0 ist, ist der Rückgabewert die erforderliche Größe für den Skriptpuffer in Zeichen, einschließlich eines beendenden NULL-Zeichens. Die Skriptanzahl ist wie oben beschrieben.

Die Funktion gibt 0 zurück, wenn sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen zu erhalten, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER \_ BADDB. Die Funktion konnte nicht auf die Daten zugreifen. Diese Situation sollte normalerweise nicht auftreten und in der Regel auf eine fehlerhafte Installation, ein Datenträgerproblem oder deren Probleme hindeutet.
-   FEHLER: \_ NICHT \_ GENÜGEND PUFFER. Eine angegebene Puffergröße war nicht groß genug, oder sie wurde fälschlicherweise auf **NULL festgelegt.**
-   FEHLER \_ \_ UNGÜLTIGE FLAGS. Die für Flags angegebenen Werte waren ungültig.
-   FEHLER \_ \_ UNGÜLTIGER PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Diese Funktion ist im Rahmen einer Strategie zur Entschärfung von Sicherheitsproblemen im Zusammenhang mit internationalisierten Domänennamen [(IDNs) nützlich.](handling-internationalized-domain-names--idns.md)

Die Skriptermittlung basiert auf den Skriptwerten, die vom Unicode-Konsortium in veröffentlicht wurden, mit der Ausnahme, dass die nicht zugewiesenen Zeichen den Wert <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> "Zzzz" (UNASSIGNED) anstelle von "Zyyy" (COMMON) haben.

Im Folgenden finden Sie einige Beispiele für das Verhalten dieser Funktion:



Eingabezeichenfolge

*dwFlags*

*lpScripts*

Skripts

Microsoft.com

0

Latn;

Lateinisch

Microsoft.com

GSS \_ ALLOW \_ INHERITED \_ COMMON

Latn; Zyyy;

Lateinisch + Allgemein

${ROWSPAN2}$Ni {REMOVE}$  

004E 0069 0241 006F

${ROWSPAN2}$GSS \_ \_ GEERBTEN \_ COMMON${REMOVE}$ ZULASSEN  

${ROWSPAN2}$Latn;${REMOVE}$  

${ROWSPAN2}$Latin${REMOVE}$  

Verwendet LATIN SMALL LETTER N MIT TILDE

${ROWSPAN2}$Ni {REMOVE}$  

004E 0069 006E 0303 006F

${ROWSPAN2}$GSS \_ \_ GEERBTEN \_ COMMON${REMOVE}$ ZULASSEN  

${ROWSPAN2}$Latn; Qaii;${REMOVE}$  

${ROWSPAN2}$Latin + Inherited${REMOVE}$  

Verwendet COMBINING TILDE

${ROWSPAN2}$Sp beif${REMOVE}$  

0053 0070 043e 043e 0066

${ROWSPAN2}$0${REMOVE}$  

${ROWSPAN2}$Latn; Cyrl;${REMOVE}$  

${ROWSPAN2}$Latin + Kyrillisch${REMOVE}$  

Verwendet KYRILLISCH KLEINBUCHSTABEN O



U+f000

0

Zzzz;

Nicht zugewiesen



U+f000

GSS \_ ALLOW \_ INHERITED \_ COMMON

Zzzz;

Nicht zugewiesen



 

Die erforderliche Headerdatei und DLL sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN)-Entschärfungs-APIs",](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) der im [MSDN Download Center verfügbar ist.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                        |
| Verteilbare Komponente<br/>          | Entschärfungs-APIs von Microsoft Internationalized Domain Name (IDN) unter Windows XP (SP2 oder höher), Windows Server 2003 (SP1 oder höher) oder Windows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprachen](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Behandeln von internationalisierten Domänennamen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 

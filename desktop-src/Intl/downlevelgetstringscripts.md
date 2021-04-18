---
description: Stellt eine Liste der in der angegebenen Unicode-Zeichenfolge verwendeten Skripts bereit.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Downlevelgetstringscripts-Funktion (idndl. h)
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
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350875"
---
# <a name="downlevelgetstringscripts-function"></a>Downlevelgetstringscripts-Funktion

Stellt eine Liste der in der angegebenen Unicode-Zeichenfolge verwendeten Skripts bereit.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung von erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**getstringscripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)aufrufen.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Flags, die Optionen für das Abrufen von Skripts angeben.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ zulassen \_ vererbte \_ Common**</dt> </dl> | Rufen Sie die Skriptinformationen "qaii" (geerbt) und "zyyy" (Common) ab. Dieser Wert hat keine Auswirkung auf die Verarbeitung nicht zugewiesener Zeichen. Diese Zeichen in der Eingabe Zeichenfolge bewirken immer, dass ein "ZZZZ" (nicht zugewiesenes Skript) in der Skript Zeichenfolge angezeigt wird.<br/> |



 

> [!Note]  
> Standardmäßig ignoriert diese Funktion alle geerbten oder allgemeinen Zeichen in der Unicode-Eingabe Zeichenfolge. Wenn GSS \_ Allow \_ geerbte \_ Common nicht festgelegt ist, wird weder "qaii" noch "zyyy" in der Skript Zeichenfolge angezeigt, auch wenn die Eingabe Zeichenfolge solche Zeichen enthält. Wenn GSS \_ \_ die Vererbung von Vererbung zulassen \_ festgelegt ist und die Eingabe Zeichenfolge geerbte und/oder gemeinsame Zeichen enthält, werden "qaii" und/oder "zyyy" in der Skript Zeichenfolge angezeigt. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

 

</dd> <dt>

*lpString* \[ in\]
</dt> <dd>

Zeiger auf die zu analysierende Unicode-Zeichenfolge.

</dd> <dt>

*cchString* \[ in\]
</dt> <dd>

Größe (in Zeichen) der Unicode-Zeichenfolge, die von *lpString* angegeben wird. Die Anwendung legt diesen Parameter auf-1 fest, wenn die Zeichenfolge NULL-terminiert ist. Wenn die Anwendung diesen Parameter auf 0 festlegt, ruft die Funktion eine NULL-Unicode-Zeichenfolge (L " \\ 0") in *lpscripts* ab und gibt 1 zurück.

</dd> <dt>

*lpscripts* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion eine auf NULL endende Zeichenfolge abruft, die eine Liste von Skripts mit der in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)verwendeten 4-Zeichen-Notation darstellt. Jeder Skript Name besteht aus vier lateinischen Zeichen, und die Namen werden in alphabetischer Reihenfolge abgerufen. Auf jeden Namen, einschließlich des letzten, folgt ein Semikolon.

Alternativ kann dieser Parameter **null** enthalten, wenn *cchscripts* auf 0 festgelegt ist. In diesem Fall gibt die-Funktion die erforderliche Größe für den Skript Puffer zurück.

</dd> <dt>

*cchscripts* \[ in\]
</dt> <dd>

Größe in Zeichen für den Skript Puffer, der von *lpscripts* angegeben wird.

Alternativ kann die Anwendung diesen Parameter auf 0 festlegen. In diesem Fall ruft die Funktion **null** in *lpscripts* ab und gibt die erforderliche Größe für den Skript Puffer zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Zeichen zurück, die im Ausgabepuffer abgerufen wurden, einschließlich eines abschließenden NULL-Zeichens, wenn erfolgreich und *cchscripts* auf einen Wert ungleich 0 (null) festgelegt ist. Die-Funktion gibt 1 zurück, um anzugeben, dass kein Skript gefunden wurde, z. b. wenn die Eingabe Zeichenfolge nur gängige oder geerbte Zeichen enthält und GSS zulassen, dass \_ \_ geerbte \_ Common nicht festgelegt ist. Da jedes gefundene Skript fünf Zeichen (vier Zeichen + Trennzeichen) hinzufügt, stellt eine einfache mathematische Operation die Skript Anzahl als (Rückgabe \_ Code-1)/5 bereit.

Wenn die Funktion erfolgreich ist und der Wert von *cchscripts* 0 ist, ist der Rückgabewert die erforderliche Größe (in Zeichen einschließlich eines abschließenden NULL-Zeichens) für den Skript Puffer. Die Skript Anzahl ist wie oben beschrieben.

Die Funktion gibt 0 zurück, wenn Sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ baddb. Die Funktion konnte nicht auf die Daten zugreifen. Diese Situation sollte normalerweise nicht eintreten, und weist in der Regel auf eine fehlerhafte Installation, ein Datenträger Problem oder das like hin.
-   Fehler \_ beim \_ Puffer. Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.
-   \_ungültige \_ Flags. Die für Flags angegebenen Werte waren ungültig.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist als Teil einer Strategie zum mindern von Sicherheitsproblemen im Zusammenhang mit [internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)nützlich.

Die Skript Bestimmung basiert auf den vom Unicode-Konsortium in veröffentlichten Skript Werten <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , mit dem Unterschied, dass die nicht zugewiesenen Zeichen den Wert "ZZZZ" (nicht zugewiesen) anstelle von "zyyy" (Common) aufweisen.

Im folgenden finden Sie einige Beispiele für das Verhalten dieser Funktion:



Eingabezeichenfolge

*dwFlags*

*lpscripts*

Skripts

Microsoft.com

0

Latn

Lateinisch

Microsoft.com

GSS \_ zulassen \_ vererbte \_ Common

Latn Zyyy;

Lateinisch und allgemein

$ {ROWSPAN2} $NI ño $ {Remove} $  

004e 0069 0241 006f

$ {ROWSPAN2} $GSS \_ \_ vererbte \_ Allgemeine $ {Remove} $ zulassen  

$ {ROWSPAN2} $Latn; $ {Remove} $  

$ {ROWSPAN2} $Latin $ {Remove} $  

Verwendet lateinischen kleinen Buchstaben N mit Tilde

$ {ROWSPAN2} $NI ño $ {Remove} $  

004e 0069 006e 0303 006f

$ {ROWSPAN2} $GSS \_ \_ vererbte \_ Allgemeine $ {Remove} $ zulassen  

$ {ROWSPAN2} $Latn; Qaii; $ {Remove} $  

$ {ROWSPAN2} $Latin + geerbt $ {Remove} $  

Verwendet das Kombinieren von Tilde

$ {ROWSPAN2} $SP ůf $ {Remove} $  

0053 0070 043e 043e 0066

$ {ROWSPAN2} $0 $ {Remove} $  

$ {ROWSPAN2} $Latn; Cyrl; $ {Remove} $  

$ {ROWSPAN2} $Latin + Cyrillic $ {Remove} $  

Verwendet den kyrillischen kleinen Buchstaben O



U + F000

0

Zzzz

Nicht zugewiesen



U + F000

GSS \_ zulassen \_ vererbte \_ Common

Zzzz

Nicht zugewiesen



 

Die erforderliche Header Datei und dll sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , der im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar ist.

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

[**Downlevelgetlocalescripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**Downlevelverifyscripts**](downlevelverifyscripts.md)
</dt> <dt>

[**Getstringscripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 

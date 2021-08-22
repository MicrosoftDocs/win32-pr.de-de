---
title: ADSI-Attributsyntax
description: 'Jedem Attribut im Verzeichnis ist eine Syntax zugeordnet. Beispiel: integer, string, numeric usw. ADSI definiert eine eigene Syntax, die der Syntax des nativen Verzeichnisses zugeordnet ist. In diesem Abschnitt werden die Typen von Attributsyntaxen in ADSI beschrieben.'
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- Attribute ADSI , Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 310a678c48051909e4a3e7555b9d8ff0a508c339cfcd41ed6c66286529cadde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023928"
---
# <a name="adsi-attribute-syntax"></a>ADSI-Attributsyntax

Jedem Attribut im Verzeichnis ist eine Syntax zugeordnet. Beispiel: integer, string, numeric usw. ADSI definiert eine eigene Syntax, die der Syntax des nativen Verzeichnisses zugeordnet ist. In diesem Abschnitt werden die Typen von Attributsyntaxen in ADSI beschrieben.

## <a name="distinguished-name-string"></a>Distinguished Name String


```VB
Syntax Type: ADSTYPE_DN_STRING
```



Der Distinguished Name ist nützlich, um zwei Objekte miteinander zu verknüpfen. Beispielsweise kann ein Link erstellt werden, der das Alice-Objekt zu einem Manager des Bob-Objekts macht. Wenn das Alice-Objekt an eine andere Stelle verschoben wird, wird der Managerlink zwischen Alice und Bob automatisch aktualisiert.

Der Distinguished Name muss ein gültiges Distinguished Name-Objekt enthalten. Wenn der Distinguished Name keinem gültigen vorhandenen Objekt entspricht, weisen die meisten Server die Anforderung zurück und geben einen Einschränkungsverletzungsfehler zurück.

Beispiele:


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Case Exact String und Case Ignore String


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



Case Exact String ist eine Zeichenfolge, bei der die Groß-/Kleinschreibung beachtet wird, während Die Groß-/Kleinschreibung ignorieren-Zeichenfolge eine Zeichenfolge ist, bei der die Groß-/Kleinschreibung nicht beachtet wird. Ein großer Prozentsatz der Attribute im Verzeichnis verwendet diese Syntax.

> [!Note]  
> Im Verzeichnis kann dies als Unicode-Zeichenfolge gespeichert werden. ADSI akzeptiert jedoch Unicode-Zeichenfolgen und gibt diese zurück.

 

Beispiel:


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a>Druckbare Zeichenfolge


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



Diese Syntax wird für Attribute mit Zeichenfolgenwerten verwendet, bei denen Groß- und Kleinbuchstaben für Vergleiche als ungleich angesehen werden, z. B. stimmen "FABRIKAM" und "Fabrikam" nicht überein. ADSI akzeptiert alle Inhalte für eine druckbare Zeichenfolge. es wird nicht versucht, zu überprüfen, ob sie tatsächlich druckbar sind.

## <a name="numeric-string"></a>Numerische Zeichenfolge


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



In dieser Syntax stimmen Zeichenfolgen wie in Druckbare Zeichenfolge überein, mit der Ausnahme, dass alle Leerzeichen in Vergleichen ignoriert werden. ADSI führt keine Wertüberprüfung durch, um sicherzustellen, dass nur Ziffern und Leerzeichen in Werten dieser Syntax angezeigt werden. Active Directory akzeptiert alle Inhalte für eine numerische Zeichenfolge. es wird nicht überprüft, ob die Zeichen numerisch sind.

## <a name="utc-time"></a>UTC-Zeit


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Diese Syntax speichert Datum und Uhrzeit in einer einzelnen Zeichenfolge. Das Zeichenfolgenformat besteht aus drei verketteten Teilen: (1) YYMMDD; (2) HHMM oder HHMMSS (beide sind akzeptabel); und (3) "Z", um anzugeben, dass die angegebene Zeit Greenwich Mean Time (GMT) ist, oder "+/-HHMM", um anzugeben, dass die angegebene Zeit Ortszeit mit der angegebenen Differenz von GMT ist. Der differenzielle Wert basiert auf der Formel GMT=Local+differential.

> [!Note]  
> Die ersten beiden Ziffern des Jahres werden nicht in dieser Zeichenfolge gespeichert.

 

Beispiele für rechtliche Werte sind "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130". Diese Zeichenfolge wird als SINGLE-Byte-ASCII-Zeichen gespeichert, und es wird keine Codepagenummer mit ihr gespeichert.

Obwohl die Sortierung unterstützt wird, erfolgt dies nur als Ascii-Zeichenfolgensortierung, bei der die Groß-/Kleinschreibung nicht beachtet wird, und nicht durch eine ordnungsgemäße Interpretation der Bedeutung der Zeichenfolgen.

Jeder gültige Zeichenfolgenwert wird akzeptiert. Es wird nicht versucht, sicherzustellen, dass die Zeichenfolge eine gültige Zeitzeichenfolge enthält.

## <a name="generalized-time"></a>Generalisierte Zeit


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Wenn ein neues Attribut zum Speichern von Zeitwerten definiert wird, sollte die GeneralizedTime-Syntax verwendet werden. Die GeneralizedTime-Syntax verwendet vier Zeichen, um das Jahr anstelle von zwei Zeichen darzustellen, wie bei UTCTime.

Das Format für die GeneralizedTime-Syntax lautet "YYYYMMDDHHMMSS.0Z". Ein Beispiel für einen akzeptablen Wert ist "20010928060000.0Z". "Z" gibt kein Zeitdifferenzial an. Active Directory speichert Datum/Uhrzeit als Greenwich Mean Time (GMT). Wenn kein Zeitdifferenzial angegeben wird, ist GMT die Standardeinstellung.

Wenn die Zeit in einer anderen Zeitzone als GMT angegeben wird, wird die Differenz zwischen der Zeitzone und GMT nicht an "Z" im Format "YYYYMMDHHMMSS.0 \[ +/- \] HHMM" angefügt. Ein Beispiel für einen zulässigen Wert ist "20010928060000.0+0200".

Der differenzielle Wert basiert auf der Formel GMT=Local+differential.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory akzeptiert nur einen 32-Bit-Wert mit Vorzeichen für diese Syntax. 0 (null) wird als **FALSE** und alle Werte ungleich 0 (null) als **TRUE** behandelt.

## <a name="integer"></a>Integer


```VB
Syntax Type: ADSTYPE_INTEGER
```



Ein numerischer 32-Bit-Wert mit Vorzeichen.

## <a name="large-integer"></a>Große ganze Zahl


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Ein numerischer 64-Bit-Wert mit Vorzeichen. Große ganze Zahlen werden tatsächlich als COM-Objekte auf der [**IADsLargeInteger-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) implementiert. Die **Methoden HighPart** und **LowPart** werden verwendet, um auf die beiden 32-Bit-Hälften des großen ganzzahligen Werts zuzugreifen.

Beispiel:


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Oktettzeichenfolge


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Eine Oktettzeichenfolge wird als variantes Bytearray zurückgegeben. Dies besteht aus einer Größenanzahl (Anzahl von Oktetten), gefolgt von einer Reihe von Oktetten. Ein Oktett ist ein 8-Bit-Byte, sodass eine Reihe von Oktetten eine Zeichenfolge von Binärdaten ist.

## <a name="object-class"></a>Objektklasse


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



Die Objektklasse ist ein eindeutiger Objektbezeichner für eine angegebene Schemaklasse. Die Klasse jeder Objektinstanz wird durch das **objectClass-Attribut** identifiziert. Bei der Erstellung können Sie nie eine Objektklasse ändern. **objectClass** ist ein Attribut mit mehreren Werten. Sie listet die spezifische Klasse des Objekts und die Klassen aller strukturellen oder abstrakten Klassen auf, von denen die spezifische Klasse abgeleitet wurde. Dies schließt Top ein, die Klasse, von der letztendlich alle anderen Klassen abgeleitet werden. Active Directory listet keine zusätzlichen Klassen im **objectClass-Attribut** auf.

## <a name="security-descriptor"></a>Sicherheitsbeschreibung


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



Zugriffsberechtigungen definieren, welche Fähigkeiten ein Sicherheitsprinzipal hat, wenn er versucht, einen Vorgang für ein Active Directory-Objekt auszuführen. Eine Sicherheitsbeschreibung beschreibt die Zugriffssteuerungsinformationen, die einem Objekt zugeordnet sind.

Der Sicherheitsdeskriptor wird als Eigenschaft eines Verzeichnisobjekts in der **nTSecurityDescriptor-Eigenschaft** gespeichert. Wenn ein authentifizierter Benutzer versucht, auf ein Verzeichnisobjekt zuzugreifen, bestimmt der Verzeichnisserver den Zugriff, der dem Benutzer basierend auf dem Objektsicherheitsdeskriptor gewährt oder verweigert wird.

Die [**ADS \_ SD \_ \_ CONTROL-ENUM-Enumeration**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) gibt Steuerungsflags für einen Sicherheitsdeskriptor an.

Das folgende Codebeispiel zeigt, wie Sie einen Sicherheitsdeskriptor abrufen.


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Syntax für Active Directory-Attribute](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[Auswählen einer Syntax](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[Angeben von Vergleichswerten](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 
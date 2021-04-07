---
title: ADSI-Attribut Syntax
description: Jedes Attribut im Verzeichnis verfügt über eine zugeordnete Syntax. Beispielsweise "Integer", "String", "numeric" usw. ADSI definiert eine eigene Syntax, die der systemeigenen Verzeichnis Syntax zuordnet. In diesem Abschnitt werden die Typen der Attribut Syntax in ADSI beschrieben.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- Attribute ADSI, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730216"
---
# <a name="adsi-attribute-syntax"></a>ADSI-Attribut Syntax

Jedes Attribut im Verzeichnis verfügt über eine zugeordnete Syntax. Beispielsweise "Integer", "String", "numeric" usw. ADSI definiert eine eigene Syntax, die der systemeigenen Verzeichnis Syntax zuordnet. In diesem Abschnitt werden die Typen der Attribut Syntax in ADSI beschrieben.

## <a name="distinguished-name-string"></a>Distinguished Name-Zeichenfolge


```VB
Syntax Type: ADSTYPE_DN_STRING
```



Der Distinguished Name ist nützlich zum Verknüpfen von zwei-Objekten. Beispielsweise kann ein Link erstellt werden, der das Alice-Objekt zu einem Vorgesetzten des Bob-Objekts macht. Wenn das Alice-Objekt an eine andere Stelle verschoben wird, wird der Manager-Link zwischen Alice und Bob automatisch aktualisiert.

Der Distinguished Name muss ein gültiges Distinguished Name-Objekt enthalten. Wenn der Distinguished Name keinem gültigen vorhandenen Objekt entspricht, wird die Anforderung von den meisten Servern abgelehnt, und es wird ein Einschränkungs Verletzungs Fehler zurückgegeben.

Beispiele:


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Exakte Groß-und Kleinschreibung Zeichenfolge ignorieren


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



Die Groß-und Kleinschreibung ist eine Zeichenfolge, bei der die Groß-/Kleinschreibung ignoriert wird. Ein großer Prozentsatz der Attribute im Verzeichnis verwendet diese Syntax.

> [!Note]  
> Das Verzeichnis speichert dies möglicherweise als Unicode-Zeichenfolge. Allerdings akzeptiert ADSI Unicode-Zeichen folgen und gibt diese zurück.

 

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



Diese Syntax wird für Attribute mit Zeichen folgen Werten verwendet, bei denen groß-und Kleinbuchstaben für Vergleiche als ungleich betrachtet werden, z. b. "Fabrikam" und "Fabrikam" stimmen nicht ab. ADSI akzeptiert alle Inhalte für eine druckbare Zeichenfolge. Es wird nicht versucht, zu überprüfen, ob Sie tatsächlich druckbar sind.

## <a name="numeric-string"></a>Numerische Zeichenfolge


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



In dieser Syntax Stimmen Zeichen folgen wie in der druckbaren Zeichenfolge ab, mit dem Unterschied, dass alle Leerzeichen in Vergleichen ignoriert werden. ADSI führt keine Wert Überprüfung durch, um sicherzustellen, dass nur Ziffern und Leerzeichen in den Werten dieser Syntax angezeigt werden. Active Directory nimmt jeglichen Inhalt für eine numerische Zeichenfolge an. Es wird nicht überprüft, ob die Zeichen numerisch sind.

## <a name="utc-time"></a>UTC-Zeit


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Diese Syntax speichert das Datum und die Uhrzeit in einer einzelnen Zeichenfolge. Das Zeichen folgen Format besteht aus drei verketteten Teilen: (1) YYMMDD; (2) HHMM oder HHMMSS (beides ist akzeptabel); und (3) "Z", um anzugeben, dass die angegebene Zeit "Greenwich Mean Time (GMT)" oder "+/-hhmm" ist, um anzugeben, dass die angegebene Zeit Ortszeit mit dem angegebenen differenziellen Wert von GMT ist. Die differenzielle Abhängigkeit basiert auf der Formel: GMT = local + Differential.

> [!Note]  
> Die ersten beiden Ziffern des Jahres werden nicht in dieser Zeichenfolge gespeichert.

 

Einige Beispiele für zulässige Werte sind "9101311455z", "910131145503z", "9101314455-0500", "910131145503 + 0130". Diese Zeichenfolge wird als Einzel Byte-ASCII-Zeichen gespeichert, und es wird keine Code Page Nummer gespeichert.

Obwohl die Sortierung unterstützt wird, wird Sie nur als Zeichen folgen Sortierung ohne Berücksichtigung der Groß-und Kleinschreibung durchgeführt, nicht durch eine ordnungsgemäße Interpretation der Bedeutung der Zeichen folgen.

Jeder gültige Zeichen folgen Wert wird akzeptiert. Es wird kein Versuch unternommen, sicherzustellen, dass die Zeichenfolge eine gültige Zeit Zeichenfolge enthält.

## <a name="generalized-time"></a>Generalisierte Zeit


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Wenn ein neues Attribut zum Speichern von Zeitwerten definiert wird, sollte die verallgemeinzedtime-Syntax verwendet werden. Die verallgemeinzedtime-Syntax verwendet vier Zeichen, um das Jahr anstelle von zwei Zeichen wie bei utcTime darzustellen.

Das Format der verallgemeinzedtime-Syntax lautet "YYYYMMDDHHMMSS. 0z". Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 z". "Z" weist auf keine Zeit differenzielle Abweichung hin. Active Directory speichert Datum/Uhrzeit als Greenwich Mean Time (GMT). Wenn keine Zeit differenzielle Angabe angegeben ist, ist GMT die Standardeinstellung.

Wenn die Uhrzeit in einer anderen Zeitzone als GMT angegeben wird, wird die Differenz zwischen der Zeitzone und der GMT an die Zeichenfolge angefügt, nicht an "Z" in der Form "YYYYMMDDHHMMSS. 0 \[ +/- \] hhmm". Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 + 0200".

Die differenzielle Abhängigkeit basiert auf der Formel: GMT = local + Differential.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory akzeptiert nur einen signierten 32-Bit-Wert für diese Syntax. Er verarbeitet NULL als **false** und alle Werte ungleich NULL als **true**.

## <a name="integer"></a>Integer


```VB
Syntax Type: ADSTYPE_INTEGER
```



Ein numerischer 32-Bit-Wert mit Vorzeichen.

## <a name="large-integer"></a>Große ganze Zahl


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Ein numerischer 64-Bit-Wert mit Vorzeichen. Große ganze Zahlen werden tatsächlich als COM-Objekte in der [**iadslargeingeteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) -Schnittstelle implementiert. Die **highpart** -und **LowPart** -Methoden werden verwendet, um auf die 2 32-Bit-Hälften des großen ganzzahligen Werts zuzugreifen.

Beispiel:


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Oktett-Zeichenfolge


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Eine Oktett-Zeichenfolge wird als Variant-Bytearray zurückgegeben. Diese besteht aus einer Größen Anzahl (Anzahl von Oktette), gefolgt von einer Reihe von Oktets. Ein Oktett ist ein 8-Bit-Byte, sodass eine Reihe von Oktette eine Zeichenfolge aus Binärdaten ist.

## <a name="object-class"></a>Objektklasse


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



Objektklasse ist ein eindeutiger Objekt Bezeichner für eine bestimmte Schema Klasse. Die Klasse der einzelnen Objektinstanzen wird durch das **objectClass** -Attribut identifiziert. Wenn Sie erstellt werden, können Sie eine Objektklasse nie ändern. **objectClass** ist ein Attribut mit mehreren Werten. Sie listet die spezifische Klasse des-Objekts und die Klassen aller strukturellen oder abstrakten Klassen auf, von denen die jeweilige Klasse abgeleitet wurde. Dies umfasst Top, die Klasse, von der alle anderen Klassen letztendlich abgeleitet werden. Active Directory listet keine Erweiterungs Klassen im **objectClass** -Attribut auf.

## <a name="security-descriptor"></a>Sicherheitsbeschreibung


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



Zugriffsrechte definieren, welche Möglichkeiten ein Sicherheits Prinzipal hat, wenn er versucht, einen Vorgang für ein Active Directory Objekt auszuführen. In einer Sicherheits Beschreibung werden die einem Objekt zugeordneten Zugriffs Steuerungsinformationen beschrieben.

Die Sicherheits Beschreibung wird als Eigenschaft eines Verzeichnis Objekts in der **ntSecurityDescriptor** -Eigenschaft gespeichert. Wenn ein authentifizierter Benutzer versucht, auf ein Verzeichnis Objekt zuzugreifen, bestimmt der Verzeichnisserver den Zugriff, der dem Benutzer basierend auf der Objekt Sicherheits Beschreibung erteilt oder verweigert wird.

Die Enumeration der [**ADS \_ SD- \_ Steuer \_**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) Element Enumeration gibt Steuerungsflags für einen Sicherheits Deskriptor an.

Im folgenden Codebeispiel wird gezeigt, wie eine Sicherheits Beschreibung abgerufen wird.


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

[Syntaxen für Active Directory Attribute](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[Auswählen einer Syntax](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[Angeben von Vergleichswerten](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 
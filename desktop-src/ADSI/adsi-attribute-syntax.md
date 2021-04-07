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
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="72707-107">ADSI-Attribut Syntax</span><span class="sxs-lookup"><span data-stu-id="72707-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="72707-108">Jedes Attribut im Verzeichnis verfügt über eine zugeordnete Syntax.</span><span class="sxs-lookup"><span data-stu-id="72707-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="72707-109">Beispielsweise "Integer", "String", "numeric" usw.</span><span class="sxs-lookup"><span data-stu-id="72707-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="72707-110">ADSI definiert eine eigene Syntax, die der systemeigenen Verzeichnis Syntax zuordnet.</span><span class="sxs-lookup"><span data-stu-id="72707-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="72707-111">In diesem Abschnitt werden die Typen der Attribut Syntax in ADSI beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72707-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="72707-112">Distinguished Name-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72707-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="72707-113">Der Distinguished Name ist nützlich zum Verknüpfen von zwei-Objekten.</span><span class="sxs-lookup"><span data-stu-id="72707-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="72707-114">Beispielsweise kann ein Link erstellt werden, der das Alice-Objekt zu einem Vorgesetzten des Bob-Objekts macht.</span><span class="sxs-lookup"><span data-stu-id="72707-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="72707-115">Wenn das Alice-Objekt an eine andere Stelle verschoben wird, wird der Manager-Link zwischen Alice und Bob automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="72707-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="72707-116">Der Distinguished Name muss ein gültiges Distinguished Name-Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="72707-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="72707-117">Wenn der Distinguished Name keinem gültigen vorhandenen Objekt entspricht, wird die Anforderung von den meisten Servern abgelehnt, und es wird ein Einschränkungs Verletzungs Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72707-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="72707-118">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="72707-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="72707-119">Exakte Groß-und Kleinschreibung Zeichenfolge ignorieren</span><span class="sxs-lookup"><span data-stu-id="72707-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="72707-120">Die Groß-und Kleinschreibung ist eine Zeichenfolge, bei der die Groß-/Kleinschreibung ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="72707-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="72707-121">Ein großer Prozentsatz der Attribute im Verzeichnis verwendet diese Syntax.</span><span class="sxs-lookup"><span data-stu-id="72707-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="72707-122">Das Verzeichnis speichert dies möglicherweise als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="72707-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="72707-123">Allerdings akzeptiert ADSI Unicode-Zeichen folgen und gibt diese zurück.</span><span class="sxs-lookup"><span data-stu-id="72707-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="72707-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="72707-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="72707-125">Druckbare Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72707-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="72707-126">Diese Syntax wird für Attribute mit Zeichen folgen Werten verwendet, bei denen groß-und Kleinbuchstaben für Vergleiche als ungleich betrachtet werden, z. b. "Fabrikam" und "Fabrikam" stimmen nicht ab.</span><span class="sxs-lookup"><span data-stu-id="72707-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="72707-127">ADSI akzeptiert alle Inhalte für eine druckbare Zeichenfolge. Es wird nicht versucht, zu überprüfen, ob Sie tatsächlich druckbar sind.</span><span class="sxs-lookup"><span data-stu-id="72707-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="72707-128">Numerische Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72707-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="72707-129">In dieser Syntax Stimmen Zeichen folgen wie in der druckbaren Zeichenfolge ab, mit dem Unterschied, dass alle Leerzeichen in Vergleichen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="72707-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="72707-130">ADSI führt keine Wert Überprüfung durch, um sicherzustellen, dass nur Ziffern und Leerzeichen in den Werten dieser Syntax angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="72707-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="72707-131">Active Directory nimmt jeglichen Inhalt für eine numerische Zeichenfolge an. Es wird nicht überprüft, ob die Zeichen numerisch sind.</span><span class="sxs-lookup"><span data-stu-id="72707-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="72707-132">UTC-Zeit</span><span class="sxs-lookup"><span data-stu-id="72707-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="72707-133">Diese Syntax speichert das Datum und die Uhrzeit in einer einzelnen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="72707-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="72707-134">Das Zeichen folgen Format besteht aus drei verketteten Teilen: (1) YYMMDD; (2) HHMM oder HHMMSS (beides ist akzeptabel); und (3) "Z", um anzugeben, dass die angegebene Zeit "Greenwich Mean Time (GMT)" oder "+/-hhmm" ist, um anzugeben, dass die angegebene Zeit Ortszeit mit dem angegebenen differenziellen Wert von GMT ist.</span><span class="sxs-lookup"><span data-stu-id="72707-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="72707-135">Die differenzielle Abhängigkeit basiert auf der Formel: GMT = local + Differential.</span><span class="sxs-lookup"><span data-stu-id="72707-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="72707-136">Die ersten beiden Ziffern des Jahres werden nicht in dieser Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72707-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="72707-137">Einige Beispiele für zulässige Werte sind "9101311455z", "910131145503z", "9101314455-0500", "910131145503 + 0130".</span><span class="sxs-lookup"><span data-stu-id="72707-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="72707-138">Diese Zeichenfolge wird als Einzel Byte-ASCII-Zeichen gespeichert, und es wird keine Code Page Nummer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72707-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="72707-139">Obwohl die Sortierung unterstützt wird, wird Sie nur als Zeichen folgen Sortierung ohne Berücksichtigung der Groß-und Kleinschreibung durchgeführt, nicht durch eine ordnungsgemäße Interpretation der Bedeutung der Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="72707-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="72707-140">Jeder gültige Zeichen folgen Wert wird akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="72707-140">Any valid string value is accepted.</span></span> <span data-ttu-id="72707-141">Es wird kein Versuch unternommen, sicherzustellen, dass die Zeichenfolge eine gültige Zeit Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="72707-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="72707-142">Generalisierte Zeit</span><span class="sxs-lookup"><span data-stu-id="72707-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="72707-143">Wenn ein neues Attribut zum Speichern von Zeitwerten definiert wird, sollte die verallgemeinzedtime-Syntax verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72707-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="72707-144">Die verallgemeinzedtime-Syntax verwendet vier Zeichen, um das Jahr anstelle von zwei Zeichen wie bei utcTime darzustellen.</span><span class="sxs-lookup"><span data-stu-id="72707-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="72707-145">Das Format der verallgemeinzedtime-Syntax lautet "YYYYMMDDHHMMSS. 0z".</span><span class="sxs-lookup"><span data-stu-id="72707-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="72707-146">Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 z".</span><span class="sxs-lookup"><span data-stu-id="72707-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="72707-147">"Z" weist auf keine Zeit differenzielle Abweichung hin.</span><span class="sxs-lookup"><span data-stu-id="72707-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="72707-148">Active Directory speichert Datum/Uhrzeit als Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="72707-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="72707-149">Wenn keine Zeit differenzielle Angabe angegeben ist, ist GMT die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="72707-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="72707-150">Wenn die Uhrzeit in einer anderen Zeitzone als GMT angegeben wird, wird die Differenz zwischen der Zeitzone und der GMT an die Zeichenfolge angefügt, nicht an "Z" in der Form "YYYYMMDDHHMMSS. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="72707-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="72707-151">Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="72707-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="72707-152">Die differenzielle Abhängigkeit basiert auf der Formel: GMT = local + Differential.</span><span class="sxs-lookup"><span data-stu-id="72707-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="72707-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="72707-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="72707-154">Active Directory akzeptiert nur einen signierten 32-Bit-Wert für diese Syntax.</span><span class="sxs-lookup"><span data-stu-id="72707-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="72707-155">Er verarbeitet NULL als **false** und alle Werte ungleich NULL als **true**.</span><span class="sxs-lookup"><span data-stu-id="72707-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="72707-156">Integer</span><span class="sxs-lookup"><span data-stu-id="72707-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="72707-157">Ein numerischer 32-Bit-Wert mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="72707-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="72707-158">Große ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="72707-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="72707-159">Ein numerischer 64-Bit-Wert mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="72707-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="72707-160">Große ganze Zahlen werden tatsächlich als COM-Objekte in der [**iadslargeingeteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="72707-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="72707-161">Die **highpart** -und **LowPart** -Methoden werden verwendet, um auf die 2 32-Bit-Hälften des großen ganzzahligen Werts zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="72707-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="72707-162">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="72707-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="72707-163">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72707-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="72707-164">Eine Oktett-Zeichenfolge wird als Variant-Bytearray zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72707-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="72707-165">Diese besteht aus einer Größen Anzahl (Anzahl von Oktette), gefolgt von einer Reihe von Oktets.</span><span class="sxs-lookup"><span data-stu-id="72707-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="72707-166">Ein Oktett ist ein 8-Bit-Byte, sodass eine Reihe von Oktette eine Zeichenfolge aus Binärdaten ist.</span><span class="sxs-lookup"><span data-stu-id="72707-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="72707-167">Objektklasse</span><span class="sxs-lookup"><span data-stu-id="72707-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="72707-168">Objektklasse ist ein eindeutiger Objekt Bezeichner für eine bestimmte Schema Klasse.</span><span class="sxs-lookup"><span data-stu-id="72707-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="72707-169">Die Klasse der einzelnen Objektinstanzen wird durch das **objectClass** -Attribut identifiziert.</span><span class="sxs-lookup"><span data-stu-id="72707-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="72707-170">Wenn Sie erstellt werden, können Sie eine Objektklasse nie ändern.</span><span class="sxs-lookup"><span data-stu-id="72707-170">When created, you can never change an object class.</span></span> <span data-ttu-id="72707-171">**objectClass** ist ein Attribut mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="72707-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="72707-172">Sie listet die spezifische Klasse des-Objekts und die Klassen aller strukturellen oder abstrakten Klassen auf, von denen die jeweilige Klasse abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="72707-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="72707-173">Dies umfasst Top, die Klasse, von der alle anderen Klassen letztendlich abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="72707-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="72707-174">Active Directory listet keine Erweiterungs Klassen im **objectClass** -Attribut auf.</span><span class="sxs-lookup"><span data-stu-id="72707-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="72707-175">Sicherheitsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="72707-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="72707-176">Zugriffsrechte definieren, welche Möglichkeiten ein Sicherheits Prinzipal hat, wenn er versucht, einen Vorgang für ein Active Directory Objekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="72707-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="72707-177">In einer Sicherheits Beschreibung werden die einem Objekt zugeordneten Zugriffs Steuerungsinformationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72707-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="72707-178">Die Sicherheits Beschreibung wird als Eigenschaft eines Verzeichnis Objekts in der **ntSecurityDescriptor** -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72707-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="72707-179">Wenn ein authentifizierter Benutzer versucht, auf ein Verzeichnis Objekt zuzugreifen, bestimmt der Verzeichnisserver den Zugriff, der dem Benutzer basierend auf der Objekt Sicherheits Beschreibung erteilt oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="72707-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="72707-180">Die Enumeration der [**ADS \_ SD- \_ Steuer \_**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) Element Enumeration gibt Steuerungsflags für einen Sicherheits Deskriptor an.</span><span class="sxs-lookup"><span data-stu-id="72707-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="72707-181">Im folgenden Codebeispiel wird gezeigt, wie eine Sicherheits Beschreibung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="72707-181">The following code example shows how to obtain a security descriptor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="72707-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72707-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72707-183">Syntaxen für Active Directory Attribute</span><span class="sxs-lookup"><span data-stu-id="72707-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="72707-184">Auswählen einer Syntax</span><span class="sxs-lookup"><span data-stu-id="72707-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="72707-185">Angeben von Vergleichswerten</span><span class="sxs-lookup"><span data-stu-id="72707-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 
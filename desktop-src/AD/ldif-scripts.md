---
title: LDIF-Skripts
description: Beim LDAP-Datenaustausch Format (LDIF) handelt es sich um einen IETF-Standard (Internet Engineering Task Force), der definiert, wie Verzeichnis Daten zwischen Verzeichnisservern, die LDAP-Dienstanbieter verwenden, importiert und exportiert werden.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- LDIF-Skripts Active Directory
- LDIF-Skripts Active Directory, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948457"
---
# <a name="ldif-scripts"></a><span data-ttu-id="f1b9c-105">LDIF-Skripts</span><span class="sxs-lookup"><span data-stu-id="f1b9c-105">LDIF Scripts</span></span>

<span data-ttu-id="f1b9c-106">Beim LDAP-Datenaustausch Format (LDIF) handelt es sich um einen IETF-Standard (Internet Engineering Task Force), der definiert, wie Verzeichnis Daten zwischen Verzeichnisservern, die LDAP-Dienstanbieter verwenden, importiert und exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-106">The LDAP Data Interchange Format (LDIF) is an Internet Engineering Task Force (IETF) standard that defines how to import and export directory data between directory servers that use LDAP service providers.</span></span> <span data-ttu-id="f1b9c-107">Windows 2000 und Windows Server 2003 enthalten ein Befehlszeilenprogramm Ldifde, das zum Importieren von Verzeichnis Objekten in Active Directory Domain Services mithilfe von LDIF-Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-107">Windows 2000 and Windows Server 2003 include a command-line utility, LDIFDE, which can be used to import directory objects into Active Directory Domain Services using LDIF files.</span></span> <span data-ttu-id="f1b9c-108">Mit LDIFDE können Sie einen Filter auf eine bestimmte Zeichenfolge festlegen, um Verzeichnisobjekte in Active Directory Domain Services als LDIF-Dateien zu suchen und aufzulisten, die problemlos von Schema Administratoren gelesen werden können.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-108">LDIFDE enables you to set a filter to a specific string in order to search for and list directory objects in Active Directory Domain Services as LDIF files which can be easily read by schema administrators.</span></span>

<span data-ttu-id="f1b9c-109">Wenn eine Unicode-Datei importiert wird, importiert LDIF de die Datei als Unicode, wenn Sie den Unicode-Bezeichner am Anfang der Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-109">When importing a Unicode file, LDIFDE imports the file as Unicode if it contains the Unicode identifier at the beginning of the file.</span></span> <span data-ttu-id="f1b9c-110">Wenn Sie eine Datei als Unicode importieren möchten, wenn Sie den Unicode-Bezeichner nicht am Anfang der Datei enthält, können Sie den Schalter-u verwenden, um zu erzwingen, dass Sie als Unicode importiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-110">If you wish to import a file as Unicode when it does not contain the Unicode identifier at the beginning of the file, you can use the -u switch in order to force it to be imported as Unicode.</span></span>

<span data-ttu-id="f1b9c-111">Der Standardmodus für den Export von Dateien ist ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-111">The default mode for exporting files is ANSI.</span></span> <span data-ttu-id="f1b9c-112">Wenn Unicode-Einträge vorhanden sind, werden diese in das Base 64-Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-112">If there are Unicode entries, they will be converted into base 64 format.</span></span> <span data-ttu-id="f1b9c-113">Um eine Datei in das Unicode-Format zu exportieren, verwenden Sie den Schalter-u.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-113">To export a file into Unicode format, use the -u switch.</span></span>

<span data-ttu-id="f1b9c-114">Eine LDIF-Datei muss Schema Änderungen anwenden, wenn Abhängigkeiten zwischen den hinzugefügten Attributen bestehen.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-114">An LDIF file must apply schema changes when there are dependencies between the attributes that are added.</span></span> <span data-ttu-id="f1b9c-115">Beispielsweise sollten vorwärts Verknüpfungs Attribute vor dem entsprechenden Backlinkattribut hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-115">For example, forward link attributes should be added before the corresponding back link attribute.</span></span> <span data-ttu-id="f1b9c-116">Sie müssen den Schema Cache auch aktualisieren, bevor Sie Klassen hinzufügen, die von Attributen oder Klassen abhängen, die zuvor im LDIF-Skript hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-116">You must also update the schema cache before adding classes that depend on attributes or classes added earlier in the LDIF script.</span></span> <span data-ttu-id="f1b9c-117">Weitere Informationen finden Sie im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-117">For more information, see the following code example.</span></span>

<span data-ttu-id="f1b9c-118">Beachten Sie, dass Sie für binäre Werte die Werte als Base64 codieren müssen.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-118">Be aware that for binary values, you must encode the values as base64.</span></span> <span data-ttu-id="f1b9c-119">Base64-Codierung ist in IETF RFC 2045, Abschnitt 6,8, definiert.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-119">Base64 encoding is defined in IETF RFC 2045, Section 6.8.</span></span>

<span data-ttu-id="f1b9c-120">Weitere Informationen zum Format von LDIF-Dateien finden Sie im [LDAP-Datenaustauschformat (LDIF)-Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) auf der Website "Internet Engineering Task Force".</span><span class="sxs-lookup"><span data-stu-id="f1b9c-120">For more information about the format of LDIF files, see [The LDAP Data Interchange Format (LDIF) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) on the Internet Engineering Task Force website.</span></span>

## <a name="ntds-specific-ldif-changetypes"></a><span data-ttu-id="f1b9c-121">NTDS-spezifische "LDIF"-ChangeTypes</span><span class="sxs-lookup"><span data-stu-id="f1b9c-121">NTDS-specific LDIF changetypes</span></span>

<span data-ttu-id="f1b9c-122">Es ist besser, ntdsschema \* -ChangeTypes zu verwenden, anstatt LDIFDE-k aufzurufenden.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-122">It is better to use ntdsSchema\* changetypes rather than calling ldifde -k.</span></span> <span data-ttu-id="f1b9c-123">Die Option "-k" von ldisde ignoriert einen größeren Satz von LDAP-Fehlern.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-123">The -k option of ldifde ignores a larger set of LDAP errors.</span></span> <span data-ttu-id="f1b9c-124">Die komplette Liste der ignorierten Fehler lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f1b9c-124">The complete list of ignored errors is as follows:</span></span>

-   <span data-ttu-id="f1b9c-125">Das Objekt ist bereits ein Mitglied der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-125">The object is already a member of the group.</span></span>
-   <span data-ttu-id="f1b9c-126">Eine Objektklassen Verletzung (d. h. die angegebene Objektklasse ist nicht vorhanden), wenn das importierte Objekt keine anderen Attribute hat.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-126">An object class violation (meaning the specified object class does not exist), if the object being imported has no other attributes.</span></span>
-   <span data-ttu-id="f1b9c-127">das Objekt ist bereits vorhanden (**LDAP ist \_ bereits \_ vorhanden**).</span><span class="sxs-lookup"><span data-stu-id="f1b9c-127">object already exists (**LDAP\_ALREADY\_EXISTS**)</span></span>
-   <span data-ttu-id="f1b9c-128">Einschränkungs Verletzung **( \_ \_ Verletzung der LDAP-Einschränkung**)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-128">constraint violation (**LDAP\_CONSTRAINT\_VIOLATION**)</span></span>
-   <span data-ttu-id="f1b9c-129">Attribut oder Wert bereits vorhanden (**LDAP- \_ Attribut \_ oder \_ Wert \_ vorhanden**)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-129">attribute or value already exists (**LDAP\_ATTRIBUTE\_OR\_VALUE\_EXISTS**)</span></span>
-   <span data-ttu-id="f1b9c-130">kein solches Objekt (**LDAP \_ - \_ Objekt nicht solches \_ Objekt**)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-130">no such object (**LDAP\_NO\_SUCH\_OBJECT**)</span></span>

<span data-ttu-id="f1b9c-131">Die folgenden ChangeTypes sind speziell für Schema Aktualisierungs Vorgänge konzipiert.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-131">The following changetypes are designed specifically for schema upgrade operations.</span></span>



| <span data-ttu-id="f1b9c-132">ChangeType</span><span class="sxs-lookup"><span data-stu-id="f1b9c-132">Changetype</span></span>                      | <span data-ttu-id="f1b9c-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1b9c-133">Description</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b9c-134">**ntdsschemaadd**</span><span class="sxs-lookup"><span data-stu-id="f1b9c-134">**ntdsSchemaAdd**</span></span><br/>    | <span data-ttu-id="f1b9c-135">**ntdsschemaadd** entspricht **Add** in einer LDIF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-135">**ntdsSchemaAdd** corresponds to **add** in an LDIF file.</span></span> <span data-ttu-id="f1b9c-136">Der einzige Unterschied ist, dass **ntdsschemaadd** bewirkt, dass LDIFDE einen **Add** -Vorgang überspringt, wenn das Objekt bereits im Schema vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-136">The only difference is that **ntdsSchemaAdd** would cause ldifde to skip an **add** operation if the object already exists in the schema.</span></span> <span data-ttu-id="f1b9c-137">(**LDAP ist \_ bereits \_ vorhanden** und wird ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-137">(**LDAP\_ALREADY\_EXISTS** is ignored.)</span></span><br/>                                   |
| <span data-ttu-id="f1b9c-138">**ntdsschemamodify**</span><span class="sxs-lookup"><span data-stu-id="f1b9c-138">**ntdsSchemaModify**</span></span><br/> | <span data-ttu-id="f1b9c-139">**ntdsschemamodify** entspricht **Modify** in einer LDIF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-139">**ntdsSchemaModify** corresponds to **modify** in an LDIF file.</span></span> <span data-ttu-id="f1b9c-140">Der einzige Unterschied ist, dass **ntdsschemamodify** bewirken würde, dass ldifde **einen Änderungs** Vorgang überspringt, wenn das Objekt nicht im Schema gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-140">The only difference is that **ntdsSchemaModify** would cause ldifde to skip an **modify** operation if the object is not found in the schema.</span></span> <span data-ttu-id="f1b9c-141">(**LDAP wird \_ nicht \_ dieses \_ Objekt** ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-141">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="f1b9c-142">**ntdsschemadelete**</span><span class="sxs-lookup"><span data-stu-id="f1b9c-142">**ntdsSchemaDelete**</span></span><br/> | <span data-ttu-id="f1b9c-143">**ntdsschemadelete** entspricht **Delete** in einer LDIF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-143">**ntdsSchemaDelete** corresponds to **delete** in an LDIF file.</span></span> <span data-ttu-id="f1b9c-144">Der einzige Unterschied ist, dass **ntdsschemadelete** bewirken würde, dass LDIFDE einen **Lösch** Vorgang überspringt, wenn das Objekt nicht im Schema gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-144">The only difference is that **ntdsSchemaDelete** would cause ldifde to skip an **delete** operation if the object is not found in the schema.</span></span> <span data-ttu-id="f1b9c-145">(**LDAP wird \_ nicht \_ dieses \_ Objekt** ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-145">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="f1b9c-146">**ntdsschemamodrdn**</span><span class="sxs-lookup"><span data-stu-id="f1b9c-146">**ntdsSchemaModRdn**</span></span><br/> | <span data-ttu-id="f1b9c-147">**ntdsschemamodrdn** entspricht in einer LDIF-Datei der Datei " **mudrdn** ".</span><span class="sxs-lookup"><span data-stu-id="f1b9c-147">**ntdsSchemaModRdn** corresponds to **modrdn** in an LDIF file.</span></span> <span data-ttu-id="f1b9c-148">Der einzige Unterschied ist, dass **ntdsschemamodrdn** bewirken würde, dass LDIFDE einen Vorgang vom Datentyp "Modify-Relative-Distinguished Name" überspringt, wenn das Objekt im Schema nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-148">The only difference is that **ntdsSchemaModRdn** would cause ldifde to skip a modify-relative-distinguished-name operation if the object is not found in the schema.</span></span> <span data-ttu-id="f1b9c-149">(**LDAP wird \_ nicht \_ dieses \_ Objekt** ignoriert.)</span><span class="sxs-lookup"><span data-stu-id="f1b9c-149">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/> |



 

## <a name="example"></a><span data-ttu-id="f1b9c-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f1b9c-150">Example</span></span>

<span data-ttu-id="f1b9c-151">Das folgende Codebeispiel enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f1b9c-151">The following code example includes:</span></span>

-   <span data-ttu-id="f1b9c-152">Myschemaext. ldf ist ein LDIF-Skript, das neue Attribute und Klassen enthält.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-152">Myschemaext.ldf is an LDIF script that contains new attributes and classes.</span></span> <span data-ttu-id="f1b9c-153">Beachten Sie, dass es sich bei dieser Datei um eine geänderte Version der Datei handelt, die aus Lgetattcls.vbs generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-153">Be aware that this file is a modified version of the file generated from Lgetattcls.vbs.</span></span> <span data-ttu-id="f1b9c-154">Beachten Sie auch, dass das **My-Test-Attribute-DN-FL** -Attribut vor **My-Test-Attribute-DN-BL** verschoben wurde, da der Backlink (**My-Test-Attribute-DN-BL**) vom Forward-Link (**My-Test-Attribute-DN-FL**) abhängt.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-154">Also be aware that the **My-Test-Attribute-DN-FL** attribute was moved ahead of **My-Test-Attribute-DN-BL** because the back link (**My-Test-Attribute-DN-BL**) is dependent on the forward link (**My-Test-Attribute-DN-FL**).</span></span> <span data-ttu-id="f1b9c-155">Außerdem wird das Attribut " **schemaUpdateNow** Operational" an zwei Stellen festgelegt, um Aktualisierungen des Schema Caches zu initiieren, damit abhängige Attribute und Klassen zum Hinzufügen der beiden Klassen im Skript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-155">Furthermore, the **schemaUpdateNow** operational attribute is set in two places to trigger updates of the schema cache so that dependent attributes and classes will be available for adding the two classes in the script.</span></span>
    > [!Note]  
    > <span data-ttu-id="f1b9c-156">Informationen zur Quelle der ID in den linkid:-Anweisungen finden Sie im Thema Abrufen [einer Link-ID](obtaining-a-link-id.md) .</span><span class="sxs-lookup"><span data-stu-id="f1b9c-156">See the topic [Obtaining a Link ID](obtaining-a-link-id.md) for information about the source of the ID in the linkID: statements.</span></span>

     

-   <span data-ttu-id="f1b9c-157">Lgetattcls.vbs ist eine VBScript-Datei, die das LDIF-Skript generiert, das als Ausgangspunkt für die Datei "myschemaext. ldf" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-157">Lgetattcls.vbs is a VBScript file that generates the LDIF script used as the starting point for the Myschemaext.ldf.</span></span> <span data-ttu-id="f1b9c-158">Beachten Sie, dass der aktuelle Schema Pfad durch "CN = Schema, CN = Configuration, DC = myorg, DC = com" ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-158">Be aware that the current schema path is replaced by CN=Schema,CN=Configuration,DC=myorg,DC=com.</span></span> <span data-ttu-id="f1b9c-159">Sie können DC = myorg, DC = com ersetzen, um den Distinguished Name (DN) für die Veröffentlichung im LDIF-Skript widerzuspiegeln, um sicherzustellen, dass LSETATTCLS.VBS die Änderung in seinem **sfromdn** widerspiegelt, sodass der korrekte DN beim Anwenden des LDIF-Skripts ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-159">You can replace DC=myorg,DC=com to reflect the distinguished name (DN) to publish in the LDIF script  ensure that LSETATTCLS.VBS reflects the change in its **sFromDN** so that the correct DN is replaced when the LDIF script is applied.</span></span> <span data-ttu-id="f1b9c-160">Beachten Sie außerdem, dass das Skript ein Präfix verwendet, um die Klassen und Attribute zu suchen, die Sie auch definieren und ein Präfix für alle Klassen und Attribute verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-160">Also be aware that the script uses a prefix to find the classes and attributes you should also define and use a prefix for all your classes and attributes.</span></span> <span data-ttu-id="f1b9c-161">Weitere Informationen finden Sie unter [Benennen von Attributen und Klassen](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f1b9c-161">For more information, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span> <span data-ttu-id="f1b9c-162">Außerdem gibt das Skript nur die erforderlichen Attribute für die Objekte **attributeSchema** und **classSchema** in der LDIF-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-162">In addition, the script outputs only the necessary attributes for the **attributeSchema** and **classSchema** objects to the LDIF file.</span></span>
-   <span data-ttu-id="f1b9c-163">Lsetattcls.vbs ist eine VBScript-Datei, die das Skript myschemaext. ldf verwendet, um die neuen Attribute und Klassen im Skript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-163">Lsetattcls.vbs is a VBScript file that uses the Myschemaext.ldf script to add the new attributes and classes in the script.</span></span> <span data-ttu-id="f1b9c-164">Stellen Sie sicher, dass der Schema Master vor dem Ausführen des Skripts in geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1b9c-164">Ensure that the schema master is able to be written to before running the script.</span></span>

## <a name="myschemaextldf"></a><span data-ttu-id="f1b9c-165">Myschemaext. LDF</span><span class="sxs-lookup"><span data-stu-id="f1b9c-165">MYSCHEMAEXT.LDF</span></span>

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a><span data-ttu-id="f1b9c-166">LGETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="f1b9c-166">LGETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a><span data-ttu-id="f1b9c-167">LSETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="f1b9c-167">LSETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 






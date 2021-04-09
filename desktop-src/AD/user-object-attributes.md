---
title: Benutzerobjekt Attribute
description: Ein Benutzerobjekt verfügt über mehrere Attribute. In diesem Abschnitt werden die von Windows, Verwaltungs Tools und Windows-Adressbuch (WAB) verwendeten Schlüssel Attribute dokumentiert. Es werden nicht alle Attribute beschrieben. viele Attribute werden nicht für das User-Objekt verwendet.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Benutzerobjekt Attribute ad
- Benutzer-AD, Benutzerobjekt Attribute
- Objekte, AD, Benutzer, Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948539"
---
# <a name="user-object-attributes"></a><span data-ttu-id="71cba-108">Benutzerobjekt Attribute</span><span class="sxs-lookup"><span data-stu-id="71cba-108">User Object Attributes</span></span>

<span data-ttu-id="71cba-109">Ein Benutzerobjekt verfügt über mehrere Attribute.</span><span class="sxs-lookup"><span data-stu-id="71cba-109">A user object has multiple attributes.</span></span> <span data-ttu-id="71cba-110">In diesem Abschnitt werden die von Windows, Verwaltungs Tools und Windows-Adressbuch (WAB) verwendeten Schlüssel Attribute dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="71cba-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="71cba-111">Es werden nicht alle Attribute beschrieben. viele Attribute werden nicht für das User-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="71cba-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="71cba-112">Einige Attribute werden im Verzeichnis gespeichert, z. b. [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)usw. und werden auf allen Domänen Controllern innerhalb einer Domäne repliziert.</span><span class="sxs-lookup"><span data-stu-id="71cba-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="71cba-113">Eine Teilmenge dieser Attribute wird auch in den globalen Katalog repliziert.</span><span class="sxs-lookup"><span data-stu-id="71cba-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="71cba-114">Nicht replizierte Attribute werden auf den einzelnen Domänen Controllern gespeichert, aber nicht an anderer Stelle repliziert, wie z. b. [**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastlogoff**](/windows/desktop/ADSchema/a-lastlogoff)usw.</span><span class="sxs-lookup"><span data-stu-id="71cba-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="71cba-115">Die nicht replizierten Attribute sind Attribute, die einen bestimmten Domänen Controller betreffen.</span><span class="sxs-lookup"><span data-stu-id="71cba-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="71cba-116">Beispielsweise ist **lastLogon** das letzte Datum und die Uhrzeit, zu der die Benutzer Netzwerk Anmeldung von dem jeweiligen Domänen Controller überprüft wurde, der die Eigenschaft zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="71cba-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="71cba-117">Ein Benutzerobjekt verfügt auch über konstruierte Attribute, die nicht im Verzeichnis gespeichert werden, sondern vom Domänen Controller berechnet werden, wie z. b. [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname), unter [**scheiden Name**](/windows/desktop/ADSchema/a-distinguishedname), [**zuordnungsdattributes**](/windows/desktop/ADSchema/a-allowedattributes)usw.</span><span class="sxs-lookup"><span data-stu-id="71cba-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="71cba-118">Attribute für Benutzer Objekte werden wie folgt klassifiziert:</span><span class="sxs-lookup"><span data-stu-id="71cba-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="71cba-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Basisobjekt Attribute</span><span class="sxs-lookup"><span data-stu-id="71cba-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="71cba-120">Diese Kategorie umfasst Attribute, die für alle Verzeichnisobjekte erforderlich sind, z. b. " [**objectClass**](/windows/desktop/ADSchema/a-objectclass)", " [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)" usw.</span><span class="sxs-lookup"><span data-stu-id="71cba-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="71cba-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Benennungs Attribute</span><span class="sxs-lookup"><span data-stu-id="71cba-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="71cba-122">Diese Kategorie schließt Attribute ein, die verwendet werden, um auf das Objekt zu verweisen oder es zu identifizieren, z.b. " [**identifishedname**](/windows/desktop/ADSchema/a-distinguishedname)", " [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)", " [**objectSID**](/windows/desktop/ADSchema/a-objectsid)" usw.</span><span class="sxs-lookup"><span data-stu-id="71cba-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="71cba-123">Weitere Informationen zu Benennungs Attributen für Benutzer Objekte finden Sie unter [Benutzer Benennungs Attribute](naming-properties.md).</span><span class="sxs-lookup"><span data-stu-id="71cba-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="71cba-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Sicherheits Attribute</span><span class="sxs-lookup"><span data-stu-id="71cba-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="71cba-125">Diese Kategorie umfasst Attribute für Anmelde-und Zugriffs Steuerung.</span><span class="sxs-lookup"><span data-stu-id="71cba-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="71cba-126">Weitere Informationen zu Sicherheits Attributen für Benutzer Objekte finden Sie unter [Benutzer Sicherheits Attribute](security-properties.md).</span><span class="sxs-lookup"><span data-stu-id="71cba-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="71cba-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Adressbuch Attribute</span><span class="sxs-lookup"><span data-stu-id="71cba-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="71cba-128">Diese Kategorie umfasst Attribute für e-Mail-und Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="71cba-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="71cba-129">Weitere Informationen zu Adressbuch Attributen für Benutzer Objekte finden Sie unter [User Address Book-Attribute](address-book-properties.md).</span><span class="sxs-lookup"><span data-stu-id="71cba-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="71cba-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Anwendungsspezifische Attribute</span><span class="sxs-lookup"><span data-stu-id="71cba-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="71cba-131">Diese Kategorie umfasst benutzerspezifische Konfigurationsdaten für bestimmte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="71cba-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="71cba-132">Weitere Informationen zum Lesen und Ändern von Attributen für ein Benutzerobjekt finden Sie unter [Lesen und Schreiben von Attributen von Objekten in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="71cba-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="71cba-133">Weitere Informationen über die User-Klasse, einschließlich einer kompletten Liste der Attribute " [**mayare**](/windows/desktop/ADSchema/a-maycontain) " und " [**mustattribute**](/windows/desktop/ADSchema/a-mustcontain) " der Klasse, finden Sie unter [**User**](/windows/desktop/ADSchema/c-user).</span><span class="sxs-lookup"><span data-stu-id="71cba-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="71cba-134">Festlegen von Kenn Wörtern</span><span class="sxs-lookup"><span data-stu-id="71cba-134">Setting Passwords</span></span>

<span data-ttu-id="71cba-135">Das Kennwort für einen Benutzer kann nicht direkt geändert werden, da dies das Senden eines unverschlüsselten Kennworts über das Netzwerk einschließen würde.</span><span class="sxs-lookup"><span data-stu-id="71cba-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="71cba-136">Um das Kennwort für einen Benutzer festzulegen, ist es erforderlich, die [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) -oder die [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) -Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="71cba-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="71cba-137">Die **IADsUser. ChangePassword** -Methode wird verwendet, wenn die Anwendung es dem Benutzer gestattet, Ihr eigenes Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="71cba-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="71cba-138">Die **IADsUser. SetPassword** -Methode wird verwendet, wenn die Anwendung einem Administrator das Zurücksetzen eines Kennworts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="71cba-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 
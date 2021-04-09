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
# <a name="user-object-attributes"></a>Benutzerobjekt Attribute

Ein Benutzerobjekt verfügt über mehrere Attribute. In diesem Abschnitt werden die von Windows, Verwaltungs Tools und Windows-Adressbuch (WAB) verwendeten Schlüssel Attribute dokumentiert. Es werden nicht alle Attribute beschrieben. viele Attribute werden nicht für das User-Objekt verwendet.

Einige Attribute werden im Verzeichnis gespeichert, z. b. [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)usw. und werden auf allen Domänen Controllern innerhalb einer Domäne repliziert. Eine Teilmenge dieser Attribute wird auch in den globalen Katalog repliziert.

Nicht replizierte Attribute werden auf den einzelnen Domänen Controllern gespeichert, aber nicht an anderer Stelle repliziert, wie z. b. [**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastlogoff**](/windows/desktop/ADSchema/a-lastlogoff)usw. Die nicht replizierten Attribute sind Attribute, die einen bestimmten Domänen Controller betreffen. Beispielsweise ist **lastLogon** das letzte Datum und die Uhrzeit, zu der die Benutzer Netzwerk Anmeldung von dem jeweiligen Domänen Controller überprüft wurde, der die Eigenschaft zurückgibt.

Ein Benutzerobjekt verfügt auch über konstruierte Attribute, die nicht im Verzeichnis gespeichert werden, sondern vom Domänen Controller berechnet werden, wie z. b. [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname), unter [**scheiden Name**](/windows/desktop/ADSchema/a-distinguishedname), [**zuordnungsdattributes**](/windows/desktop/ADSchema/a-allowedattributes)usw.

Attribute für Benutzer Objekte werden wie folgt klassifiziert:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Basisobjekt Attribute
</dt> <dd>

Diese Kategorie umfasst Attribute, die für alle Verzeichnisobjekte erforderlich sind, z. b. " [**objectClass**](/windows/desktop/ADSchema/a-objectclass)", " [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)" usw.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Benennungs Attribute
</dt> <dd>

Diese Kategorie schließt Attribute ein, die verwendet werden, um auf das Objekt zu verweisen oder es zu identifizieren, z.b. " [**identifishedname**](/windows/desktop/ADSchema/a-distinguishedname)", " [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)", " [**objectSID**](/windows/desktop/ADSchema/a-objectsid)" usw. Weitere Informationen zu Benennungs Attributen für Benutzer Objekte finden Sie unter [Benutzer Benennungs Attribute](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Sicherheits Attribute
</dt> <dd>

Diese Kategorie umfasst Attribute für Anmelde-und Zugriffs Steuerung. Weitere Informationen zu Sicherheits Attributen für Benutzer Objekte finden Sie unter [Benutzer Sicherheits Attribute](security-properties.md).

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Adressbuch Attribute
</dt> <dd>

Diese Kategorie umfasst Attribute für e-Mail-und Benutzerdaten. Weitere Informationen zu Adressbuch Attributen für Benutzer Objekte finden Sie unter [User Address Book-Attribute](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Anwendungsspezifische Attribute
</dt> <dd>

Diese Kategorie umfasst benutzerspezifische Konfigurationsdaten für bestimmte Anwendungen.

</dd> </dl>

Weitere Informationen zum Lesen und Ändern von Attributen für ein Benutzerobjekt finden Sie unter [Lesen und Schreiben von Attributen von Objekten in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Weitere Informationen über die User-Klasse, einschließlich einer kompletten Liste der Attribute " [**mayare**](/windows/desktop/ADSchema/a-maycontain) " und " [**mustattribute**](/windows/desktop/ADSchema/a-mustcontain) " der Klasse, finden Sie unter [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Festlegen von Kenn Wörtern

Das Kennwort für einen Benutzer kann nicht direkt geändert werden, da dies das Senden eines unverschlüsselten Kennworts über das Netzwerk einschließen würde. Um das Kennwort für einen Benutzer festzulegen, ist es erforderlich, die [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) -oder die [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) -Methode zu verwenden. Die **IADsUser. ChangePassword** -Methode wird verwendet, wenn die Anwendung es dem Benutzer gestattet, Ihr eigenes Kennwort zu ändern. Die **IADsUser. SetPassword** -Methode wird verwendet, wenn die Anwendung einem Administrator das Zurücksetzen eines Kennworts ermöglicht.

 

 
---
title: Verzeichnis Objektauswahl
description: Mit dem Dialogfeld Verzeichnis Objektauswahl kann ein Benutzer ein oder mehrere Objekte aus dem globalen Katalog, einer Domäne oder einem Computer oder einer Arbeitsgruppe auswählen.
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- Verzeichnis Objektauswahl (AD)
- Objektauswahl anzeigen
- Objekte AD, Objektauswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6ba7fd053aa8ab3245bf72c693f0a887aa983
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038767"
---
# <a name="directory-object-picker"></a>Verzeichnis Objektauswahl

Mit dem Dialogfeld Verzeichnis Objektauswahl kann ein Benutzer ein oder mehrere Objekte aus dem globalen Katalog, einer Domäne oder einem Computer oder einer Arbeitsgruppe auswählen. Zu den Objekttypen, aus denen ein Benutzer auswählen kann, gehören Benutzer-, Kontakt-, Gruppen-und Computer Objekte. Weitere Informationen zu Active Directory Domain Services finden Sie unter [Active Directory Domain Services](active-directory-domain-services.md).

So zeigen Sie das Dialogfeld "Objektauswahl" an:

1.  Rufen Sie die Funktion [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**cokreateinstanceex**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) auf, um eine Instanz der [**idsobjectpicker**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker) -Schnittstelle zu erstellen.
2.  Aufrufen der [**idsobjectpicker:: Initialisieren**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) -Methode, um das Dialogfeld zu initialisieren.
3.  Aufrufen der [**idsobjectpicker:: invokedialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) -Methode, um das Dialogfeld anzuzeigen.
4.  Rufen Sie die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Instanz auf, die vom Dialogfeld Objektauswahl zurückgegeben wird, um die [**cfstr \_ DSOP \_ DS- \_ Auswahl \_ Listen**](cfstr-dsop-ds-selection-list.md) Daten abzurufen. Das Format der **cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste** in der Zwischenablage bietet einen **HGLOBAL** , der eine [**DS- \_ Auswahl \_ Listen**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) Struktur enthält. Die Struktur der **DS- \_ Auswahl \_ Liste** enthält Daten zu den Elementen, die im Dialogfeld Objektauswahl ausgewählt wurden.

Wenn die Sicherheits-ID (SID) für ein Objekt erforderlich ist, sollte diese direkt von der Objektauswahl angefordert werden, indem das **objectSID** -Attribut der Liste der Attribute hinzugefügt wird, die für das ausgewählte Objekt abgerufen werden sollen. Es wird nicht empfohlen, den zurückgegebenen Objektnamen an die Funktion [**lsalookupnames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) oder [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) zu übergeben, da die Namenssuche redundant ist und in einigen Fällen möglicherweise fehlschlägt.

Wenn ein Verweis auf ausgewählte Objekte gespeichert wird, sollte der Distinguished Name nicht gespeichert werden, da das Objekt möglicherweise verschoben, umbenannt oder aufgrund von Gebiets Schema unterschieden geändert werden kann. Für Sicherheits Prinzipale sollte die **objectSID** für das Objekt angefordert und sicher gespeichert werden. Wenn der Name des Sicherheits Prinzipals später benötigt wird, kann er mit der [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion abgerufen werden. Für alle anderen Objekte muss die **objectGUID** angefordert und gespeichert werden.

## <a name="initialization"></a>Initialisierung

Wenn das Dialogfeld Objektauswahl initialisiert wird, wird ein Satz von Bereichs Typen und Filtern angegeben. Die angegebenen Bereichs Typen bestimmen z. b. die Standorte, Domänen oder Computer, von denen aus die Benutzer Objekte auswählen können. Die Filter bestimmen die Objekttypen, die ein Benutzer aus einem bestimmten Bereichstyp auswählen kann. Weitere Informationen finden Sie weiter unten im Abschnitt Bereiche und Filter.

Standardmäßig kann ein Benutzer ein einzelnes Objekt im Dialogfeld Verzeichnis Objektauswahl auswählen. Wenn Sie mehrere Auswahlen aktivieren möchten, legen **Sie das DSOP- \_ Flag \_ MultiSelect** -Flag im **floptions** -Member der [**DSOP \_ Init \_ Info**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) -Struktur fest, wenn das Dialogfeld initialisiert wird.

## <a name="scopes-and-filters"></a>Bereiche und Filter

Die Dropdown Liste **Suchen in** enthält die Bereiche, aus denen ein Benutzer Objekte auswählen kann. Ein Bereich ist eine Domäne, ein Computer, eine Arbeitsgruppe oder ein globaler Katalog, in der Daten zu einem Satz verfügbarer Objekte gespeichert werden und der Zugriff darauf ermöglicht. Die Einträge in der Bereichs Liste hängen von den Bereichs Typen und dem Bereitstellungs Zielcomputer ab, der beim letzten Aufruf der [**idsobjectpicker:: Initialisieren**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) -Methode aufgerufen wurde, um das Dialogfeld Objektauswahl zu initialisieren.

Ein Bereichstyp ist eine generische Kategorie von Bereichen, z. b. alle Domänen in dem Unternehmen, zu denen der Zielcomputer gehört, oder der globale Katalog für das Unternehmen des Ziel Computers oder der Zielcomputer. Im Dialogfeld wird für jeden angegebenen Bereichstyp der Kontext des Bereitstellungs Ziel Computers verwendet, um die Einträge in der Bereichs Liste zu ermitteln.

Die [**idsobjectpicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) -Methode verwendet einen Zeiger auf eine [**DSOP- \_ Init- \_ Informations**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) Struktur, die ein Array von [**DSOP-Scope- \_ \_ Init \_ Info**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) -Strukturen enthält. Jeder Eintrag im **DSOP \_ Scope \_ Init \_ Info** -Array gibt einen oder mehrere Bereichs Typen sowie anwendbare Filter und andere Attribute an. Die Filter bestimmen die Objekttypen, z. b. Benutzer, Gruppen, Kontakte und Computer, die der Benutzer aus einem bestimmten Bereichstyp auswählen kann. Wenn der Benutzer einen Bereich aus der Liste auswählt, wendet das Dialogfeld die Filter für diesen Bereichstyp an, um eine Liste von Objekten anzuzeigen, aus denen der Benutzer auswählen kann.

Jede [**DSOP- \_ Bereich- \_ Init \_ Info**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) -Struktur enthält eine [**DSOP- \_ \_ Filterflags**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) -Struktur, die die Filter für diesen Bereichstyp angibt. Die **DSOP \_ - \_ Filterflags** -Struktur unterscheidet zwischen den Bereichen auf der Ebene und der untergeordneten Ebene:

-   Ein Bereich auf der Ebene ist ein globaler Katalog oder eine Domäne, die den ADSI [LDAP-Anbieter](/windows/desktop/ADSI/adsi-ldap-provider)unterstützt.
-   Ein Bereich auf der Ebene umfasst Arbeitsgruppen und alle einzelnen Computer. Im Dialogfeld wird der ADSI WinNT-Anbieter verwendet, um auf einen downlevelbereich zuzugreifen.

Es gibt zwei Sätze von Filterflags, die für die Verwendung in der [**DSOP- \_ \_ Filterflags**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) -Struktur definiert sind: eine für upebenenbereiche und eine für Bereiche mit untergeordneten Ebenen. Der **Uplevel** -Member der **DSOP \_ - \_ Filterflags** -Struktur ist eine [**DSOP- \_ Uplevel- \_ \_ Filterflags**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags) -Struktur, die die Filter für upebenenbereiche angibt. Der **fldownlevel** -Member der **DSOP \_ - \_ Filterflags** -Struktur ist ein Satz von Flags, die die Filter für downlevelbereiche angeben.

 

 
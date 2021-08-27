---
description: Ab Windows Vista verfügen viele sicherungsfähige Objekte über Methoden zum Abrufen oder Festlegen des Sicherheitsdeskriptors. Mit den entsprechenden Berechtigungen können Sie Sicherheitsbeschreibungen für sicherungsfähige Objekte lesen oder ändern.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Ändern der Zugriffssicherheit für sicherungsfähige Objekte
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050988"
---
# <a name="changing-access-security-on-securable-objects"></a>Ändern der Zugriffssicherheit für sicherungsfähige Objekte

Drucker, Dienste, Registrierungsschlüssel, DCOM-Anwendungen und WMI-Namespaces sind sicherungsfähige Objekte. Der Zugriff auf sicherungsfähige Objekte wird durch [*Sicherheitsdeskriptoren*](/windows/desktop/SecGloss/s-gly)geschützt, die die Benutzer angeben, die Zugriff haben. Ab Windows Vista verfügen viele sicherungsfähige Objekte über Methoden zum Abrufen oder Festlegen des Sicherheitsdeskriptors. Mit den entsprechenden Berechtigungen können Sie Sicherheitsbeschreibungen für sicherungsfähige Objekte lesen oder ändern. Mit diesen Methoden können Sie steuern, welche Benutzerkonten oder Gruppen Zugriff auf einen Drucker, Dienst, WMI-Namespace oder ein anderes Objekt haben. Weitere Informationen zu Sicherheitsdeskriptoren und deren Verwendung in WMI finden Sie unter [Zugriff auf sicherungsfähige WMI-Objekte.](access-to-wmi-securable-objects.md)

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Objekte und Sicherheitsbeschreibungsmethoden](#objects-and-security-descriptor-methods)
-   [Konvertieren zwischen Sicherheitsbeschreibungsformaten](#converting-between-security-descriptor-formats)
-   [Sicherheitsprobleme](#security-issues)
-   [Zugehörige Themen](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Objekte und Sicherheitsbeschreibungsmethoden

Die folgende Liste enthält die Methoden, mit denen sicherungsfähige Objekte den Sicherheitsdeskriptor lesen oder ändern können:

-   WMI-Namespaces

    Ein Anbieter kann Sicherheit einrichten, die nur bestimmten Gruppen zugriff auf die Daten in einem WMI-Namespace zulässt. Die Namespacesicherheit wird durch Methoden der [**\_ \_ SystemSecurity-Klasse**](--systemsecurity.md) gesteuert. Ab Windows Vista geben die [**Methoden GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) und [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) [**\_ \_ SecurityDescriptor-Objekte**](--securitydescriptor.md) zurück und schreiben sie. Weitere Informationen finden Sie unter [Festlegen von Namespacesicherheitsdeskriptoren.](setting-namespace-security-descriptors.md)

-   Registrierungsschlüssel

    Ab Windows Vista können Sie Registrierungsschlüssel schützen, sodass sie nicht von nicht autorisierten Benutzern geändert werden können. Die [**StdRegProv-Klasse**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt über [**die Methoden GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) und [**SetSecurityDescriptor.**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) Diese Methoden geben [**Win32 \_ SecurityDescriptor-Objekte zurück und schreiben**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) sie.

-   Drucker

    Ab Windows Vista können Sie den Zugriff auf Instanzen der [**Win32 \_ Printer-Klasse**](/windows/desktop/CIMWin32Prov/win32-printer) mithilfe der [**Methoden GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) und [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) sichern. Diese Methoden geben [**Win32 \_ SecurityDescriptor-Objekte zurück und schreiben**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) sie.

-   Dienste

    Ab Windows Vista können Sie den Zugriff auf Instanzen der [**Win32-Dienstklasse \_**](/windows/desktop/CIMWin32Prov/win32-service) mithilfe der [**Methoden GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) und [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) sichern. Diese Methoden geben [**Win32 \_ SecurityDescriptor-Objekte zurück und schreiben**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) sie.

-   DCOM-Anwendungen

    DCOM-Anwendungsinstanzen verfügen über mehrere Sicherheitsbeschreibungen. Verwenden Sie ab Windows Vista Methoden der [**Win32 \_ DCOMApplicationSetting-Klasse,**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) um die verschiedenen Sicherheitsbeschreibungen zu erhalten oder zu ändern. Sicherheitsdeskriptoren werden als Instanzen der [**Win32 \_ SecurityDescriptor-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) zurückgegeben.

    Um die Konfigurationsberechtigungen zu erhalten oder zu ändern, rufen Sie die [**Methoden GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) oder [**SetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) auf.

    Um die Zugriffsberechtigungen zu erhalten oder zu ändern, rufen Sie die [**Methoden GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) oder [**SetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) auf.

    Um die Start- und Aktivierungsberechtigungen zu erhalten oder zu ändern, rufen Sie die [**Methoden GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) oder [**SetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) auf.

-   Files

    Die [**Methoden GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) [**und SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) befinden sich in der [**Win32 \_ LogicalFileSecuritySetting-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) und nicht in der [**CIM \_ DataFile-Klasse.**](/windows/desktop/CIMWin32Prov/cim-datafile)

-   Freigaben

    Die [**Methoden GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) und [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) befinden sich in der [**Win32 \_ LogicalShareSecuritySetting-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) und nicht in der [**Win32 \_ Share-Klasse.**](/windows/desktop/CIMWin32Prov/win32-share)

> [!Note]  
> Wenn keine neue [*Security Access Control List (SACL)*](/windows/desktop/SecGloss/s-gly) in einem Aufruf einer **SetSecurityDescriptor-Methode** angegeben wird, wird die Sicherheitsbeschreibung SACL für das sicherungsfähige Zielobjekt auf **NULL** festgelegt, sodass die vorherige SACL-Einstellung nicht beibehalten wird.

 

## <a name="converting-between-security-descriptor-formats"></a>Konvertieren zwischen Sicherheitsbeschreibungsformaten

Sicherheitsdeskriptoren sind komplexe binäre Bytearrays, die normalerweise in C++ erstellt und geändert werden müssen. Nachdem Sie eine der Get-Methoden verwendet haben, um den Sicherheitsdeskriptor zu erhalten, stellt die [**Win32 \_ SecurityDescriptorHelper-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) Methoden zur Konvertierung von Sicherheitsdeskriptoren entweder in [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) oder in [**Win32 \_ SecurityDescriptor-Instanzen**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) zur Verwendung.

Sie können die Access Control Listen (ACL) einfacher in [**Win32 \_ SecurityDescriptor-Instanzen**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) oder in SDDL bearbeiten. Weitere Informationen zur Struktur und Verwendung von Sicherheitsdeskriptoren in WMI finden Sie unter [WMI-Sicherheitsdeskriptorobjekte.](wmi-security-descriptor-objects.md)

Verwenden Sie in C++ oder C# Konvertierungsfunktionen, um binäre Sicherheitsdeskriptoren in [SDDL (Security Descriptor Definition Language) zu konvertieren.](/windows/desktop/SecAuthZ/security-descriptor-definition-language) Verwenden Sie [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor,**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)um Sicherheitsdeskriptorwerte in C++-Anwendungen zu ändern.

## <a name="security-issues"></a>Sicherheitsprobleme

Es wird empfohlen, Änderungen an Sicherheitsdeskriptoren mit großer Vorsicht vorzunehmen, damit die Sicherheit des Objekts nicht beeinträchtigt wird. Beachten Sie, dass sich die Reihenfolge der Zugriffssteuerungseinträge (ACCESS Control Entries, ACEs) in einer DACL (Discretionary Access Control List) auf die Zugriffssicherheit auswirken kann. Weitere Informationen finden Sie unter [Reihenfolge der ACEs in einer DACL.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[Security Descriptor Helper-Klasse](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Bewährte Sicherheitsmethoden](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 

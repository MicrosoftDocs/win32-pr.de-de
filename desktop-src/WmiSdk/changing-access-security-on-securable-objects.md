---
description: Ab Windows Vista verfügen viele Sicherungs fähige Objekte über Methoden zum erhalten oder Festlegen der Sicherheits Beschreibung. Mit den entsprechenden Berechtigungen können Sie Sicherheits Deskriptoren für Sicherungs fähige Objekte lesen oder ändern.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Ändern der Zugriffssicherheit für Sicherungs fähige Objekte
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9682c259fc2f7e45409f7ddcaaa95dac2cba1b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353519"
---
# <a name="changing-access-security-on-securable-objects"></a>Ändern der Zugriffssicherheit für Sicherungs fähige Objekte

Drucker, Dienste, Registrierungsschlüssel, DCOM-Anwendungen und WMI-Namespaces sind Sicherungs fähige Objekte. Der Zugriff auf Sicherungs fähige Objekte wird durch [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly)geschützt, die die Benutzer angeben, die Zugriff haben. Ab Windows Vista verfügen viele Sicherungs fähige Objekte über Methoden zum erhalten oder Festlegen der Sicherheits Beschreibung. Mit den entsprechenden Berechtigungen können Sie Sicherheits Deskriptoren für Sicherungs fähige Objekte lesen oder ändern. Mit diesen Methoden können Sie steuern, welche Benutzerkonten oder-Gruppen Zugriff auf einen Drucker, einen Dienst, einen WMI-Namespace oder ein anderes Objekt haben. Weitere Informationen zu Sicherheits Beschreibungen und deren Verwendung in WMI finden [Sie unter Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Objekte und Sicherheits deskriptormethoden](#objects-and-security-descriptor-methods)
-   [Wechseln zwischen Sicherheits deskriptorformaten](#converting-between-security-descriptor-formats)
-   [Sicherheitsprobleme](#security-issues)
-   [Zugehörige Themen](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Objekte und Sicherheits deskriptormethoden

In der folgenden Liste sind die Methoden enthalten, mit denen Sicherungs fähige Objekte die Sicherheits Beschreibung lesen oder ändern können:

-   WMI-Namespaces

    Ein Anbieter kann die Sicherheit festlegen, die nur bestimmten Gruppen den Zugriff auf die Daten in einem WMI-Namespace gestattet. Die Namespace Sicherheit wird durch Methoden der [**\_ \_ System Security**](--systemsecurity.md) -Klasse gesteuert. Ab Windows Vista geben die [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) -Methode und die [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md) -Methode [**\_ \_ securityDescriptor**](--securitydescriptor.md) -Objekte zurück und schreiben Sie. Weitere Informationen finden Sie unter [Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).

-   Registrierungsschlüssel

    Ab Windows Vista können Sie Registrierungsschlüssel sichern, damit Sie nicht von unbefugten Benutzern geändert werden können. Die Klasse " [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) " hat die Methoden " [**getsecuritydescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) " und " [**SETSECURITYDESCRIPTOR**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) ". Mit diesen Methoden werden [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Objekte zurückgegeben und geschrieben.

-   Drucker

    Ab Windows Vista können Sie den Zugriff auf Instanzen der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse mithilfe der Methoden [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) und [**SETSECURITYDESCRIPTOR**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) sichern. Mit diesen Methoden werden [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Objekte zurückgegeben und geschrieben.

-   Dienste

    Ab Windows Vista können Sie den Zugriff auf Instanzen der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse mithilfe der Methoden [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) und [**SETSECURITYDESCRIPTOR**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) sichern. Mit diesen Methoden werden [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Objekte zurückgegeben und geschrieben.

-   DCOM-Anwendungen

    DCOM-Anwendungs Instanzen verfügen über mehrere Sicherheits Deskriptoren. Ab Windows Vista können Sie die Methoden der [**Win32 \_ dcomapplicationsetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) -Klasse verwenden, um die verschiedenen Sicherheits Deskriptoren zu erhalten oder zu ändern. Sicherheits Deskriptoren werden als Instanzen der Win32- [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse zurückgegeben.

    Um die Konfigurations Berechtigungen abzurufen oder zu ändern, müssen Sie die Methoden [**getconfigurationsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) oder [**setconfigurationsecuritydescriptor**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) aufrufen.

    Um die Zugriffsberechtigungen abzurufen oder zu ändern, müssen Sie die [**getaccesssecuritydescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) -Methode oder die [**setaccesssecuritydescriptor**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) -Methode aufrufen.

    Um die Start-und Aktivierungs Berechtigungen abzurufen oder zu ändern, müssen Sie die Methoden [**getlaunchsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) oder [**setlaunchsecuritydescriptor**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) aufrufen.

-   Dateien

    Die [**getsecuritydescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) -Methode und die [**SETSECURITYDESCRIPTOR**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) -Methode sind in der [**Win32 \_ logicalfilesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) -Klasse und nicht in der [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) -Klasse.

-   Freigaben

    Die [**getsecuritydescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) -Methode und die [**SETSECURITYDESCRIPTOR**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) -Methode sind in der [**Win32 \_ logicalsharesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) -Klasse und nicht in der [**Win32- \_ Freigabe**](/windows/desktop/CIMWin32Prov/win32-share) Klasse.

> [!Note]  
> Wenn eine neue [*Sicherheits Access Control Liste (SACL)*](/windows/desktop/SecGloss/s-gly) in einem Aufruf einer **SETSECURITYDESCRIPTOR** -Methode nicht angegeben wird, wird die Sicherheits Beschreibung für das Sicherungs fähige Objekt auf **null** festgelegt, sodass die vorherige SACL-Einstellung nicht beibehalten wird.

 

## <a name="converting-between-security-descriptor-formats"></a>Wechseln zwischen Sicherheits deskriptorformaten

Sicherheits Deskriptoren sind komplexe binäre Byte Arrays, die normalerweise in C++ erstellt und geändert werden müssen. Nachdem Sie eine der Get-Methoden zum Abrufen der Sicherheits Beschreibung verwendet haben, stellt die [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse Methoden bereit, die Sicherheits Deskriptoren in die [Sicherheits Deskriptor-Definitions Sprache (Security Descriptor Definition Language, SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) oder [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanzen konvertieren.

Sie können die Access Control Listen (ACL) leichter in Win32- [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanzen oder in SDDL manipulieren. Weitere Informationen zur Struktur und Verwendung von Sicherheits Deskriptoren in WMI finden Sie unter [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).

In C++ oder c# verwenden Sie Konvertierungs Funktionen, um binäre Sicherheits Deskriptoren in die [Sicherheits Deskriptor-Definitions Sprache (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)zu konvertieren. Verwenden Sie zum Ändern der sicherheitsdeskriptorwerte in C++-Anwendungen [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Sicherheitsprobleme

Es wird empfohlen, dass Änderungen an Sicherheits Beschreibungen mit großer Vorsicht durchgeführt werden, damit die Sicherheit des Objekts nicht beeinträchtigt wird. Beachten Sie, dass sich die Reihenfolge der Zugriffs Steuerungs Einträge (ACEs) in einer freigegebenen Zugriffs Steuerungs Liste (DACL) auf die Zugriffssicherheit auswirken kann. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[Hilfsklasse für Sicherheits Deskriptoren](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Bewährte Sicherheitsmethoden](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 

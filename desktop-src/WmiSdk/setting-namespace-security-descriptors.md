---
description: Sowohl C++-Anwendungen als auch Skripts, die unter einem vollständigen Administrator Konto ausgeführt werden, können eine Namespace-Sicherheits Beschreibung ändern.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Festlegen von Namespace-Sicherheits Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353972"
---
# <a name="setting-namespace-security-descriptors"></a>Festlegen von Namespace-Sicherheits Deskriptoren

Sowohl C++-Anwendungen als auch Skripts, die unter einem vollständigen Administrator Konto ausgeführt werden, können eine Namespace-Sicherheits Beschreibung ändern.

## <a name="namespace-security-descriptors"></a>Namespace-Sicherheits Deskriptoren

Jeder WMI-Namespace verfügt über eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly), die es jedem Namespace ermöglicht, eindeutige Sicherheitseinstellungen festzulegen, die festlegen, wer Zugriff auf die Namespace Daten und-Methoden hat. Weitere Informationen zur WMI-Zugriffssicherheit finden [Sie unter Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md). Der [Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md) beschreibt die Standard Sicherheitseinstellungen für WMI-Namespaces und die Sicherheitsüberwachung in WMI.

Sie können die Konto Berechtigungen für jeden WMI-Namespace im WMI-Repository (CIM) auf folgende Weise festlegen:

-   Wenn der Namespace in der MOF-Datei erstellt wird. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).
-   Manuell mit dem WMI-Steuerelement. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.
-   Programm gesteuert durch Aufrufen der Methoden der [**\_ \_ SystemSecurity**](--systemsecurity.md) -Klasse.

Die folgenden Methoden des [**\_ \_ SystemSecurity**](--systemsecurity.md) -Objekts, das mit jedem Namespace verknüpft ist, ermöglichen es Ihnen, die Sicherheit für einen Namespace zu lesen oder zu ändern.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**Getcalleraccessrights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Legt den *Rights* -Parameter als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

Ruft die Sicherheits Beschreibung für den Namespace ab, mit dem der Benutzer verbunden ist. Diese Methode gibt eine Sicherheits Beschreibung im Format des binären Byte Arrays zurück. Wenn Sie ein Skript schreiben, verwenden Sie die [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) -Methode.

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

Legt die Sicherheits Beschreibung für den Namespace fest, mit dem ein Benutzer verbunden ist. Diese Methode erfordert eine Sicherheits Beschreibung im Format des binären Byte Arrays. Wenn Sie ein Skript schreiben, verwenden Sie die [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md) -Methode.

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, der der-Instanz von [**\_ \_ SystemSecurity**](--systemsecurity.md)zugeordnet ist. Die Sicherheits Beschreibung wird als Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)zurückgegeben.

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert. Die Sicherheits Beschreibung wird durch eine Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)dargestellt.

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Ruft die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, bei denen die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Legt die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.

</dd> </dl>

Wenn Sie Skripts schreiben, verwenden Sie " [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) " und " [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md)". Sie können die-Methoden der [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse verwenden, um die Sicherheits Deskriptoren zu ändern.

Wenn Sie in C++ programmieren, können Sie die binäre Sicherheits Beschreibung mithilfe von [SDDL (Security Deskriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und Konvertierungs Methoden [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.

Beachten Sie, dass sich die [Benutzerkontensteuerung (User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) , UAC) ab Windows Vista auf den Zugriff auf WMI-Daten auswirkt und was mit dem [*WMI-Steuer*](gloss-w.md)Element konfiguriert werden kann. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 

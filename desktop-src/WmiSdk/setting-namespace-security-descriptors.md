---
description: Sowohl C++-Anwendungen als auch Skripts, die unter einem vollständigen Administratorkonto ausgeführt werden, können einen Namespacesicherheitsdeskriptor ändern.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Festlegen von Namespacesicherheitsdeskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc112376a960c3760bc51450cc30b8da3a38c24fa52e985321b2662ae319a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050298"
---
# <a name="setting-namespace-security-descriptors"></a>Festlegen von Namespacesicherheitsdeskriptoren

Sowohl C++-Anwendungen als auch Skripts, die unter einem vollständigen Administratorkonto ausgeführt werden, können einen Namespacesicherheitsdeskriptor ändern.

## <a name="namespace-security-descriptors"></a>Namespacesicherheitsdeskriptoren

Jeder WMI-Namespace verfügt über einen [*Sicherheitsdeskriptor,*](/windows/desktop/SecGloss/s-gly)der jedem Namespace eindeutige Sicherheitseinstellungen ermöglicht, die bestimmen, wer Zugriff auf die Namespacedaten und -methoden hat. Weitere Informationen zur WMI-Zugriffssicherheit finden Sie unter [Zugriff auf sicherungsfähige WMI-Objekte.](access-to-wmi-securable-objects.md) [Der Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md) beschreibt die Standardsicherheitseinstellungen für WMI-Namespaces und die Sicherheitsüberwachung in WMI.

Sie können Kontoberechtigungen für jeden WMI-Namespace im WMI-Repository (CIM) wie folgt festlegen:

-   Wenn der Namespace in der MOF-Datei erstellt wird. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit beim Erstellen des Namespaces.](setting-namespace-security-when-the-namespace-is-created.md)
-   Manuelles Verwenden des WMI-Steuerelements. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit mit dem WMI-Steuerelement](setting-namespace-security-with-the-wmi-control.md).
-   Programmgesteuert durch Aufrufen der Methoden der [**\_ \_ SystemSecurity-Klasse.**](--systemsecurity.md)

Mit den folgenden Methoden des [**\_ \_ SystemSecurity-Objekts,**](--systemsecurity.md) das jedem Namespace zugeordnet ist, können Sie die Sicherheit für einen Namespace lesen oder ändern.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Legt den *Rights-Parameter* als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

Ruft die Sicherheitsbeschreibung für den Namespace ab, mit dem der Benutzer verbunden ist. Diese Methode gibt einen Sicherheitsdeskriptor im binären Bytearrayformat zurück. Wenn Sie ein Skript schreiben, verwenden Sie die [**GetSecurityDescriptor-Methode.**](getsecuritydescriptor-method-in-class---systemsecurity-.md)

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

Legt die Sicherheitsbeschreibung (Security Descriptor, SD) für den Namespace fest, mit dem ein Benutzer verbunden ist. Diese Methode erfordert einen Sicherheitsdeskriptor im binären Bytearrayformat. Wenn Sie ein Skript schreiben, verwenden Sie die [**SetSecurityDescriptor-Methode.**](setsecuritydescriptor-method-in-class---systemsecurity.md)

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Ruft die Sicherheitsbeschreibung ab, die den Zugriff auf den WMI-Namespace steuert, der der Instanz von [**\_ \_ SystemSecurity**](--systemsecurity.md)zugeordnet ist. Der Sicherheitsdeskriptor wird als Instanz von [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)zurückgegeben.

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Schreibt eine aktualisierte Version des Sicherheitsdeskriptors, der den Zugriff auf den Drucker steuert. Der Sicherheitsdeskriptor wird durch eine Instanz von [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)dargestellt.

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Ruft die Remotezugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, auf denen die Zugriffssteuerung über Windows Sicherheitsbeschreibungen nicht verfügbar ist.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Legt die Remotezugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffssteuerung über Windows Sicherheitsbeschreibungen nicht verfügbar ist.

</dd> </dl>

Wenn Sie Skripts schreiben, verwenden [**Sie getSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) und [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md). Sie können die Methoden der [**Win32 \_ SecurityDescriptorHelper-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) verwenden, um die Sicherheitsbeschreibungen zu ändern.

Wenn Sie in C++ programmieren, können Sie den binären Sicherheitsdeskriptor mithilfe von [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und den Konvertierungsmethoden [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.

Beachten Sie, dass sich die [Benutzerkontensteuerung](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (User Account Control, UAC) ab Windows Vista auf den Zugriff auf WMI-Daten auswirkt und was mit dem [*WMI-Steuerelement*](gloss-w.md)konfiguriert werden kann. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[WMI-Sicherheitskonstanten](wmi-security-constants.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dt>

[WMI-Sicherheitsbeschreibungsobjekte](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 

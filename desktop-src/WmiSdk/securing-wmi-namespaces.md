---
description: Der Zugriff auf WMI-Namespaces und Ihre Daten wird durch Sicherheits Deskriptoren gesteuert.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Sichern von WMI-Namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349120"
---
# <a name="securing-wmi-namespaces"></a>Sichern von WMI-Namespaces

Der Zugriff auf WMI-Namespaces und Ihre Daten wird durch [*Sicherheits Deskriptoren*](gloss-s.md)gesteuert. Sie können Daten in Ihren [*Namespaces*](gloss-n.md) schützen, indem Sie die Namespace-Sicherheits Beschreibung anpassen, um zu steuern, wer Zugriff auf die Daten und Methoden hat. Weitere Informationen finden Sie unter [Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).


In den folgenden Themen wird die WMI-Namespace Sicherheit und die Steuerung des Zugriffs auf Namespaces beschrieben.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dd>

WMI-Namespace Sicherheit basiert auf standardmäßigen Windows- [*benutzersicherheitsbezeichgern*](/windows/desktop/SecGloss/s-gly) (SIDs) und Zugriffs Steuerungs Listen. Administratoren und Benutzer haben unterschiedliche Standard Berechtigungen.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dd>

Nachdem ein Namespace im WMI-Repository vorhanden ist, können Sie die Sicherheit für den Namespace ändern, indem Sie das WMI-Steuerelement verwenden oder die Methoden von [**\_ \_ SystemSecurity**](--systemsecurity.md)aufrufen.

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Eine verschlüsselte Verbindung mit einem Namespace ist erforderlich.](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

Der "Requirements **sencryption** "-Qualifizierer für einen Namespace erfordert, dass die WMI-Client Anwendung oder das Skript die Authentifizierungs Ebene verwendet, die Remote Prozedur Aufrufe verschlüsselt. Eingehende Datenanforderungen und asynchrone Rückrufe müssen verschlüsselt werden.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Einrichten der Vererbung der Namespace Sicherheit](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Sie können steuern, ob ein untergeordneter Namespace die Sicherheits Beschreibung des übergeordneten Namespaces erbt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Erstellen eines Namespace mit der WMI-API](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 

---
description: Der Zugriff auf WMI-Namespaces und deren Daten wird durch Sicherheitsbeschreibungen gesteuert.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Sichern von WMI-Namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3cdf2b6e5c5cf035fed70e3e0dd949a812505f1f1ded8f1599043cdd75ba4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992370"
---
# <a name="securing-wmi-namespaces"></a>Sichern von WMI-Namespaces

Der Zugriff auf WMI-Namespaces und deren Daten wird durch [*Sicherheitsbeschreibungen*](gloss-s.md)gesteuert. Sie können Daten in Ihren Namespaces schützen, indem Sie die [*Namespacesicherheitsbeschreibung*](gloss-n.md) anpassen, um zu steuern, wer Zugriff auf die Daten und Methoden hat. Weitere Informationen finden Sie unter [Zugriff auf sicherungsfähige WMI-Objekte.](access-to-wmi-securable-objects.md)


Die folgenden Themen beschreiben die Sicherheit von WMI-Namespaces und die Steuerung des Zugriffs auf Namespaces.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dd>

Die WMI-Namespacesicherheit basiert auf standard Windows SIDs (User [*Security Identifiers)*](/windows/desktop/SecGloss/s-gly) und Zugriffssteuerungslisten. Administratoren und Benutzer verfügen über unterschiedliche Standardberechtigungen.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Festlegen von Namespacesicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> <dd>

Nachdem ein Namespace im WMI-Repository vorhanden ist, können Sie die Sicherheit für den Namespace ändern, indem Sie das WMI-Steuerelement verwenden oder die Methoden von [**\_ \_ SystemSecurity**](--systemsecurity.md)aufrufen.

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

Der **RequiresEncryption-Qualifizierer** für einen Namespace erfordert, dass die WMI-Clientanwendung oder das WMI-Skript die Authentifizierungsebene verwendet, die Remoteprozeduraufrufe verschlüsselt. Sowohl eingehende Datenanforderungen als auch asynchrone Rückrufe müssen verschlüsselt werden.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Festlegen der Vererbung von Namespacesicherheit](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Sie können steuern, ob ein untergeordneter Namespace die Sicherheitsbeschreibung des übergeordneten Namespace erbt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Erstellen eines Namespace mit der WMI-API](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[WMI-Sicherheitsbeschreibungsobjekte](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 

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
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="48e81-103">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="48e81-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="48e81-104">Der Zugriff auf WMI-Namespaces und Ihre Daten wird durch [*Sicherheits Deskriptoren*](gloss-s.md)gesteuert.</span><span class="sxs-lookup"><span data-stu-id="48e81-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="48e81-105">Sie können Daten in Ihren [*Namespaces*](gloss-n.md) schützen, indem Sie die Namespace-Sicherheits Beschreibung anpassen, um zu steuern, wer Zugriff auf die Daten und Methoden hat.</span><span class="sxs-lookup"><span data-stu-id="48e81-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="48e81-106">Weitere Informationen finden Sie unter [Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="48e81-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="48e81-107">In den folgenden Themen wird die WMI-Namespace Sicherheit und die Steuerung des Zugriffs auf Namespaces beschrieben.</span><span class="sxs-lookup"><span data-stu-id="48e81-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="48e81-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="48e81-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="48e81-109">WMI-Namespace Sicherheit basiert auf standardmäßigen Windows- [*benutzersicherheitsbezeichgern*](/windows/desktop/SecGloss/s-gly) (SIDs) und Zugriffs Steuerungs Listen.</span><span class="sxs-lookup"><span data-stu-id="48e81-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="48e81-110">Administratoren und Benutzer haben unterschiedliche Standard Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="48e81-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="48e81-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="48e81-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="48e81-112">Nachdem ein Namespace im WMI-Repository vorhanden ist, können Sie die Sicherheit für den Namespace ändern, indem Sie das WMI-Steuerelement verwenden oder die Methoden von [**\_ \_ SystemSecurity**](--systemsecurity.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48e81-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="48e81-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Eine verschlüsselte Verbindung mit einem Namespace ist erforderlich.](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="48e81-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="48e81-114">Der "Requirements **sencryption** "-Qualifizierer für einen Namespace erfordert, dass die WMI-Client Anwendung oder das Skript die Authentifizierungs Ebene verwendet, die Remote Prozedur Aufrufe verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="48e81-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="48e81-115">Eingehende Datenanforderungen und asynchrone Rückrufe müssen verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="48e81-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="48e81-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Einrichten der Vererbung der Namespace Sicherheit](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="48e81-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="48e81-117">Sie können steuern, ob ein untergeordneter Namespace die Sicherheits Beschreibung des übergeordneten Namespaces erbt.</span><span class="sxs-lookup"><span data-stu-id="48e81-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="48e81-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48e81-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48e81-119">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="48e81-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="48e81-120">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="48e81-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="48e81-121">Erstellen eines Namespace mit der WMI-API</span><span class="sxs-lookup"><span data-stu-id="48e81-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="48e81-122">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="48e81-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 

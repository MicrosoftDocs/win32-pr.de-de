---
description: Eine Sicherheits Beschreibung enthält die Sicherheitsinformationen, die einem Sicherungs fähigen Objekt zugeordnet sind.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Sicherheitsbeschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863007"
---
# <a name="security-descriptors"></a><span data-ttu-id="3a6a2-103">Sicherheitsbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="3a6a2-103">Security Descriptors</span></span>

<span data-ttu-id="3a6a2-104">Eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) enthält die Sicherheitsinformationen, die einem Sicherungs [fähigen Objekt](securable-objects.md)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="3a6a2-105">Eine Sicherheits Beschreibung besteht aus einer [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) und den zugehörigen Sicherheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="3a6a2-106">Eine Sicherheits Beschreibung kann die folgenden Sicherheitsinformationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="3a6a2-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="3a6a2-107">[Sicherheits](security-identifiers.md) -IDs (SIDs) für den Besitzer und die primäre Gruppe eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="3a6a2-108">Eine [DACL](access-control-lists.md) , die die Zugriffsrechte angibt, die bestimmten Benutzern oder Gruppen gewährt oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="3a6a2-109">Eine [SACL](access-control-lists.md) , die die Typen von Zugriffsversuchen angibt, die Überwachungsdaten Sätze für das Objekt generieren.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="3a6a2-110">Ein Satz von Steuerungs Bits, die die Bedeutung einer Sicherheits Beschreibung oder ihrer einzelnen Member qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="3a6a2-111">Anwendungen dürfen den Inhalt einer Sicherheits Beschreibung nicht direkt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="3a6a2-112">Die Windows-API stellt Funktionen zum Festlegen und Abrufen der Sicherheitsinformationen in der Sicherheits Beschreibung eines Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="3a6a2-113">Außerdem gibt es Funktionen zum Erstellen und Initialisieren einer Sicherheits Beschreibung für ein neues-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="3a6a2-114">Anwendungen, die mit Sicherheits Deskriptoren auf Active Directory Objekten arbeiten, können die Windows-Sicherheitsfunktionen oder die von den Active Directory Service Interfaces (ADSI) bereitgestellten Sicherheits Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="3a6a2-115">Weitere Informationen zu ADSI-Sicherheits Schnittstellen finden Sie unter [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="3a6a2-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 

---
description: Sie können die Fähigkeit eines Prozesses steuern, auf Sicherungs fähige Objekte zuzugreifen oder Systemverwaltungsaufgaben auszuführen.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Angeben einer Sicherheits Beschreibung aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960748"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="09575-103">Angeben einer Sicherheits Beschreibung aus einer INF-Datei</span><span class="sxs-lookup"><span data-stu-id="09575-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="09575-104">Sie können die Fähigkeit eines Prozesses steuern, auf Sicherungs fähige Objekte zuzugreifen oder Systemverwaltungsaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="09575-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="09575-105">Ein Sicherungs fähiges Objekt ist ein Objekt, das über eine Sicherheits Beschreibung verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="09575-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="09575-106">Alle benannten Objekte sind Sicherungs fähig.</span><span class="sxs-lookup"><span data-stu-id="09575-106">All named objects are securable.</span></span> <span data-ttu-id="09575-107">Einige unbenannte Objekte (z. b. Prozess-und Thread Objekte) können auch Sicherheits Deskriptoren aufweisen.</span><span class="sxs-lookup"><span data-stu-id="09575-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="09575-108">Weitere Informationen zum Steuern des Zugriffs auf Sicherungs fähige Objekte finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="09575-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="09575-109">[Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors) enthalten die Sicherheitsinformationen, die Sicherungs fähigen Objekten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="09575-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="09575-110">Bei den meisten Sicherungs fähigen Objekten können Sie die Sicherheits Beschreibung eines Objekts im Funktionsaufruf angeben, von dem das Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="09575-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="09575-111">Sie können z. b. eine Sicherheits Beschreibung [**in den Funktionen**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "up" und " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " angeben.</span><span class="sxs-lookup"><span data-stu-id="09575-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="09575-112">Um eine Sicherheits Beschreibung aus einer INF-Datei festzulegen, fügen Sie einen von INF-Writer erstellten Sicherheitsabschnitt direkt nach dem Abschnitt hinzu, der die Datei, den Registrierungsschlüssel oder die Komponente installiert.</span><span class="sxs-lookup"><span data-stu-id="09575-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="09575-113">Der Abschnitt Security sollte eine Zeile mit der Zeichen folgen-Sicherheits Beschreibung enthalten, die das Format für [sicherheitsbeschreibungerzeichenfolgen](/windows/desktop/SecAuthZ/security-descriptor-strings)enthält.</span><span class="sxs-lookup"><span data-stu-id="09575-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="09575-114">Die Zeile sollte auch in Anführungszeichen (") eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="09575-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="09575-115">Beispielsweise würde der folgende INF-Datei Ausschnitt einen Registrierungsschlüssel erstellen, auf den nur Administratoren und das System zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="09575-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="09575-116">Beachten Sie, dass für dieses Beispiel Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="09575-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="09575-117">In diesem Fall ist die Bedeutung der Zeichenfolge, dass Administratoren über Vollzugriff verfügen, das System über Vollzugriff verfügt und der Zugriff auf alle Unterschlüssel vererbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="09575-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="09575-118">Weitere Informationen finden Sie unter [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="09575-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 

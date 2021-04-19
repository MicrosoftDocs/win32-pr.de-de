---
description: SACL für ein neues Objekt
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL für ein neues Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356526"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="ab496-103">SACL für ein neues Objekt</span><span class="sxs-lookup"><span data-stu-id="ab496-103">SACL for a New Object</span></span>

<span data-ttu-id="ab496-104">Das System verwendet den folgenden Algorithmus, um eine SACL für die meisten Typen von neuen Sicherungs fähigen Objekten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="ab496-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="ab496-105">Die SACL des Objekts ist die SACL aus der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) , die durch den Ersteller des Objekts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab496-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="ab496-106">Das System führt alle vererbbaren ACEs in der angegebenen SACL zusammen, es sei denn, das \_ geschützte SE SACL \_ -Bit wird in den Steuerungs Bits der Sicherheits Beschreibung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab496-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="ab496-107">\_ \_ Systemressourcenattribute \_ -ACEs und systemweite \_ \_ Richtlinien- \_ ID- \_ ACEs von einem übergeordneten Objekt werden mit einem neuen-Objekt zusammengeführt, auch wenn das "SE \_ SACL \_ Protected Bit" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab496-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="ab496-108">Wenn der Ersteller keine Sicherheits Beschreibung angibt, erstellt das System die SACL des Objekts aus vererbbaren ACEs.</span><span class="sxs-lookup"><span data-stu-id="ab496-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="ab496-109">Wenn keine angegebene oder geerbte SACL vorhanden ist, hat das-Objekt keine SACL.</span><span class="sxs-lookup"><span data-stu-id="ab496-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="ab496-110">Um eine SACL für ein neues Objekt anzugeben, muss für den Ersteller des Objekts die \_ Sicherheits \_ Namen [Berechtigung](privileges.md) "SE" aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ab496-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="ab496-111">Wenn die angegebene SACL für ein neues-Objekt nur das System \_ Ressourcen \_ Attribut ACEs enthält \_ , ist die Berechtigung "SE \_ Security Name" \_ nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ab496-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="ab496-112">Der Ersteller benötigt diese Berechtigung nicht, wenn die SACL des Objekts aus geerbten ACEs erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab496-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="ab496-113">Das System verwendet einen anderen Algorithmus, um eine SACL für ein neues Active Directory Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab496-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="ab496-114">Weitere Informationen finden Sie unter [Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="ab496-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 

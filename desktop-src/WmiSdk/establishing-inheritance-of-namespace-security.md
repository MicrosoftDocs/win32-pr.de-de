---
description: Sie können steuern, ob ein untergeordneter Namespace die Sicherheits Beschreibung des übergeordneten Namespaces erbt.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Einrichten der Vererbung der Namespace Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353928"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="f9550-103">Einrichten der Vererbung der Namespace Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f9550-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="f9550-104">Sie können steuern, ob ein untergeordneter Namespace die Sicherheits Beschreibung des übergeordneten Namespaces erbt.</span><span class="sxs-lookup"><span data-stu-id="f9550-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="f9550-105">WMI-Namespaces verfügen über Sicherheits Deskriptoren, die Steuern, wer auf den-Namespace und die Daten des-Namespace zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f9550-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="f9550-106">Jede Sicherheits Beschreibung verfügt über eine freigegebene Zugriffs Steuerungs Liste (DACL) und eine Sicherheits Zugriffs Steuerungs Liste (SACL).</span><span class="sxs-lookup"><span data-stu-id="f9550-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="f9550-107">Diese Listen enthalten Zugriffs Steuerungs Einträge (Access Control Entries, ACE).</span><span class="sxs-lookup"><span data-stu-id="f9550-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="f9550-108">Abhängig von den festgelegten [**Namespace-ACE-Flag-Konstanten**](namespace-ace-flag-constants.md) können Berechtigungen, die auf einen Namespace angewendet werden, von allen untergeordneten Namespaces dieses Namespace geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="f9550-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="f9550-109">Ein untergeordneter Namespace erbt die Sicherheits Beschreibung des übergeordneten Namespaces, wenn der untergeordnete Namespace erstellt wird, wenn das Flag für das **Container \_ Vererbung- \_ ACE** in der übergeordneten Namespace-Sicherheits Beschreibung ist.</span><span class="sxs-lookup"><span data-stu-id="f9550-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="f9550-110">Wenn der **Container erben, ohne dass der \_ \_ \| \_ anordnunggator \_ geerbt \_** werden soll, erbt nur der untergeordnete Namespace die Sicherheits Beschreibung, nicht die untergeordneten Namespaces.</span><span class="sxs-lookup"><span data-stu-id="f9550-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="f9550-111">Untergeordnete Namespaces können die Sicherheits Berechtigungen des übergeordneten Namespaces überschreiben, indem Sie Methoden der [**\_ \_ SystemSecurity**](--systemsecurity.md) -Klasse aufrufen, um eine neue Sicherheits Beschreibung zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f9550-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="f9550-112">Die Standard Sicherheitseinstellungen können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f9550-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="f9550-113">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md). Weitere Informationen zu DACLs finden Sie unter [Access Control Listen (ACL)](/windows/desktop/SecAuthZ/access-control-lists) und [**Namespace-ACE-Typkonstanten**](namespace-ace-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f9550-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="f9550-114">Beachten Sie, dass die Standard Berechtigungen nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f9550-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="f9550-115">Darüber hinaus wird das Flag für die **SE \_ DACL \_** -Sicherheit beim Festlegen der Sicherheits Beschreibung (SD) nicht zum Hinzufügen einer spezialisierten SD zu einem untergeordneten Namespace verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9550-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="f9550-116">Wenn Sie eine geerbte SD überschreiben möchten, legen Sie einfach einen neuen fest.</span><span class="sxs-lookup"><span data-stu-id="f9550-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="f9550-117">Wenn Sie diese SD in einem untergeordneten Namespace erben möchten, übergeben Sie das Flag **Container \_ erben- \_ ACE** in der Sicherheits Beschreibung des-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f9550-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="f9550-118">Um nur das untergeordnete Element zu erben, nicht die Nachfolger, übergeben Sie. `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="f9550-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="f9550-119">.</span><span class="sxs-lookup"><span data-stu-id="f9550-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9550-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9550-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9550-121">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="f9550-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="f9550-122">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="f9550-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 

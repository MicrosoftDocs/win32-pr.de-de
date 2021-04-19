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
# <a name="establishing-inheritance-of-namespace-security"></a>Einrichten der Vererbung der Namespace Sicherheit

Sie können steuern, ob ein untergeordneter Namespace die Sicherheits Beschreibung des übergeordneten Namespaces erbt.

WMI-Namespaces verfügen über Sicherheits Deskriptoren, die Steuern, wer auf den-Namespace und die Daten des-Namespace zugreifen kann. Jede Sicherheits Beschreibung verfügt über eine freigegebene Zugriffs Steuerungs Liste (DACL) und eine Sicherheits Zugriffs Steuerungs Liste (SACL). Diese Listen enthalten Zugriffs Steuerungs Einträge (Access Control Entries, ACE).

Abhängig von den festgelegten [**Namespace-ACE-Flag-Konstanten**](namespace-ace-flag-constants.md) können Berechtigungen, die auf einen Namespace angewendet werden, von allen untergeordneten Namespaces dieses Namespace geerbt werden. Ein untergeordneter Namespace erbt die Sicherheits Beschreibung des übergeordneten Namespaces, wenn der untergeordnete Namespace erstellt wird, wenn das Flag für das **Container \_ Vererbung- \_ ACE** in der übergeordneten Namespace-Sicherheits Beschreibung ist. Wenn der **Container erben, ohne dass der \_ \_ \| \_ anordnunggator \_ geerbt \_** werden soll, erbt nur der untergeordnete Namespace die Sicherheits Beschreibung, nicht die untergeordneten Namespaces. Untergeordnete Namespaces können die Sicherheits Berechtigungen des übergeordneten Namespaces überschreiben, indem Sie Methoden der [**\_ \_ SystemSecurity**](--systemsecurity.md) -Klasse aufrufen, um eine neue Sicherheits Beschreibung zu schreiben. Die Standard Sicherheitseinstellungen können nicht geändert werden. Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md). Weitere Informationen zu DACLs finden Sie unter [Access Control Listen (ACL)](/windows/desktop/SecAuthZ/access-control-lists) und [**Namespace-ACE-Typkonstanten**](namespace-ace-type-constants.md).

Beachten Sie, dass die Standard Berechtigungen nicht geändert werden können. Darüber hinaus wird das Flag für die **SE \_ DACL \_** -Sicherheit beim Festlegen der Sicherheits Beschreibung (SD) nicht zum Hinzufügen einer spezialisierten SD zu einem untergeordneten Namespace verwendet. Wenn Sie eine geerbte SD überschreiben möchten, legen Sie einfach einen neuen fest. Wenn Sie diese SD in einem untergeordneten Namespace erben möchten, übergeben Sie das Flag **Container \_ erben- \_ ACE** in der Sicherheits Beschreibung des-Namespace. Um nur das untergeordnete Element zu erben, nicht die Nachfolger, übergeben Sie. `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 

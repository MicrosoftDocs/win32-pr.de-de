---
description: Sie können steuern, ob ein untergeordneter Namespace die Sicherheitsbeschreibung des übergeordneten Namespace erbt.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Festlegen der Vererbung von Namespacesicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951bd5a2a14aa0a62620090d07df9bc56e8a0832674f2c1eee84369f4e2b4dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411910"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Festlegen der Vererbung von Namespacesicherheit

Sie können steuern, ob ein untergeordneter Namespace die Sicherheitsbeschreibung des übergeordneten Namespace erbt.

WMI-Namespaces verfügen über Sicherheitsbeschreibungen, die steuern, wer auf den Namespace und die Daten des Namespace zugreifen kann. Jeder Sicherheitsdeskriptor verfügt über eine DACL (Discretionary Access Control List) und eine SACL (Security Access Control List). Diese Listen enthalten Zugriffssteuerungseinträge (ACE).

Abhängig von den festgelegten [**Namespace-ACE-Flagkonstanten**](namespace-ace-flag-constants.md) können Berechtigungen, die auf einen Namespace angewendet werden, von allen untergeordneten Namespaces dieses Namespace geerbt werden. Ein untergeordneter Namespace erbt die Sicherheitsbeschreibung des übergeordneten Namespace, wenn der untergeordnete Namespace erstellt wird, wenn sich das **CONTAINER \_ INHERIT \_ ACE-Flag** im Sicherheitsdeskriptor des übergeordneten Namespace befindet. Wenn **CONTAINER INHERIT ACE NO \_ \_ \| \_ PROPOGATE \_ INHERIT \_ ACE** festgelegt ist, erbt nur der untergeordnete Namespace den Sicherheitsdeskriptor, nicht die untergeordneten Namespaces. Untergeordnete Namespaces können die Sicherheitsberechtigungen ihres übergeordneten Elements überschreiben, indem sie Methoden der [**\_ \_ SystemSecurity-Klasse**](--systemsecurity.md) aufrufen, um einen neuen Sicherheitsdeskriptor zu schreiben. Die Standardsicherheitseinstellungen können nicht geändert werden. Weitere Informationen finden Sie unter [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md). Weitere Informationen zu DACLs finden Sie unter [Access Control Listen (ACL)](/windows/desktop/SecAuthZ/access-control-lists) und [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).

Beachten Sie, dass die Standardberechtigungen nicht geändert werden können. Darüber hinaus wird das Festlegen des **\_ SE DACL \_ PROTECTED-Flags** beim Festlegen der Sicherheitsbeschreibung (SECURITY Descriptor, SD) nicht verwendet, um einem untergeordneten Namespace eine spezielle SD hinzuzufügen. Um eine geerbte SD zu überschreiben, legen Sie einfach eine neue fest. Um diese SD an einen untergeordneten Namespace zu erben, übergeben Sie das **\_ \_ ACE-Flag CONTAINER INHERIT** im Namespacesicherheitsdeskriptor. Um nur an das untergeordnete Element und nicht an die Nachfolger zu erben, übergeben Sie `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 

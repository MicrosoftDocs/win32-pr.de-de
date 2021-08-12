---
description: Die folgende Liste listet die möglichen Werte des Flags-Felds in einem WMI-Access Control Entry (ACE) auf.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Namespace-ACE-Flagkonstanten (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 7b4051a6c17e9861d656207335b2543cf7d886e74569c269df2a4f680f47fbe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555180"
---
# <a name="namespace-ace-flag-constants"></a>Ace-Flagkonstanten für Namespaces

In der folgenden Liste sind die möglichen Werte des **Felds Flags** in einem WMI-Access Control Entry (ACE) aufgeführt.

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**\_OBJEKTVERERBUNGS-ACE \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Untergeordnete Objekte, die keine Container sind, erben den ACE als effektiven ACE.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Der ACE wirkt sich sowohl auf untergeordnete Namespaces als auch auf den aktuellen Namespace aus.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO \_ PROPAGATE \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Der ACE gilt nur für den aktuellen Namespace und die unmittelbar untergeordneten Elemente .


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**\_NUR ACE ERBEN \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Der ACE gilt nur für untergeordnete Namespaces.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**GEERBTER \_ ACE**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Dies wird nicht von Clients festgelegt, sondern an Clients gemeldet, wenn die Quelle eines ACE ein übergeordneter Namespace ist.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[WMI-Sicherheitskonstanten](wmi-security-constants.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[Festlegen der Vererbung von Namespacesicherheit](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 





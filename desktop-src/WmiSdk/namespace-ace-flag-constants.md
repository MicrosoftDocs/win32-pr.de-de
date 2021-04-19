---
description: In der folgenden Liste sind die möglichen Werte des Felds Flags in einem WMI-Access Control Entry (ACE) aufgelistet.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Namespace-ACE-Flag-Konstanten (WinNT. h)
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
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370771"
---
# <a name="namespace-ace-flag-constants"></a>Namespace-ACE-Flag-Konstanten

In der folgenden Liste sind die möglichen Werte des Felds **Flags** in einem WMI-Access Control Entry (ACE) aufgelistet.

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**Objekt \_ erben ( \_ ACE)**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Untergeordnete Objekte, die nicht Container sind, erben den ACE als effektiven ACE.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**Container \_ erben ( \_ ACE)**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Der ACE wirkt sich auf untergeordnete Namespaces und den aktuellen Namespace aus.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**kein \_ propagieren- \_ \_ ACE erben**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Der ACE gilt nur für den aktuellen Namespace und die unmittelbar untergeordneten Elemente.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**\_nur \_ ACE erben**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Der ACE gilt nur für untergeordnete Namespaces.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**geerbte \_ ACE**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Dies wird nicht von Clients festgelegt, sondern an Clients gemeldet, wenn die Quelle eines ACE ein übergeordneter Namespace ist.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WinNT. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Einrichten der Vererbung der Namespace Sicherheit](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 





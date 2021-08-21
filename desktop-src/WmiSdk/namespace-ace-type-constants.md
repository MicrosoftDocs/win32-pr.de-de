---
description: Das Feld Typ in einem Zugriffssteuerungseintrag (ACE), das bestimmt, ob der ACE ein ACE ist, der den Zugriff zulässt oder verweigert.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Namespace-ACE-Typkonstanten (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 99eb4f19cd4e669e7bb5f791b1e45246bf3e29d9ef20df003cefe21284f5ac63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817996"
---
# <a name="namespace-ace-type-constants"></a>Ace-Typkonstanten für Namespaces

Das **Feld Typ** in einem Zugriffssteuerungseintrag (ACE), das bestimmt, ob der ACE ein ACE ist, der den Zugriff zulässt oder verweigert.

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Ermöglichen**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Der ACE ermöglicht den Zugriff auf den Namespace.


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Verweigern**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Der ACE verweigert den Zugriff auf den Namespace.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Sicherheitskonstanten](wmi-security-constants.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[Festlegen der Vererbung von Namespacesicherheit](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 





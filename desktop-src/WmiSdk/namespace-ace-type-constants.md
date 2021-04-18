---
description: Das typanfeld in einem Zugriffs Steuerungs Eintrag (Access Control Entry, ACE), der bestimmt, ob der ACE ein ACE ist, der den Zugriff zulässt oder verweigert.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Namespace-ACE-Typkonstanten (WinNT. h)
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
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371496"
---
# <a name="namespace-ace-type-constants"></a>Namespace-ACE-Typkonstanten

Das **typanfeld** in einem Zugriffs Steuerungs Eintrag (Access Control Entry, ACE), der bestimmt, ob der ACE ein ACE ist, der den Zugriff zulässt oder verweigert.

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Ließen**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Der ACE ermöglicht den Zugriff auf den-Namespace.


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Men**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Der ACE verweigert den Zugriff auf den-Namespace.


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

 

 





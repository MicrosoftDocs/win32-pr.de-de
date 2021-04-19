---
description: Das Client-Objekt stellt eine Beziehung zwischen einer Komponente und einem Client Produkt dar.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Clientobjekt.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361933"
---
# <a name="client-object"></a>Clientobjekt.

Das Client-Objekt stellt eine Beziehung zwischen einer Komponente und einem Client Produkt dar.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieses Objekt ist ab Windows Installer 5,0 verfügbar.

## <a name="members"></a>Member

Das **Client** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Client** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                 | BESCHREIBUNG                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**Componentcode**](client-componentcode.md)<br/> | Der Komponenten Code der betreffenden Komponente.<br/> |
| [**Kontext**](client-context.md)<br/>             | Der Kontext des Produkts.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | Das Client Produkt der betreffenden Komponente.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | Die Benutzer-SID für die Komponente.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 oder höher.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IClient ist definiert als 000c1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden der Automatisierungsschnittstelle](using-the-automation-interface.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





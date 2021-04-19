---
description: Das Festlegen dieser Eigenschaft entspricht dem Festlegen der transformsatsource-Richtlinien Richtlinie, mit dem Unterschied, dass der Bereich abweicht.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Transformsatsource (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367824"
---
# <a name="transformsatsource-property"></a>Transformsatsource (Eigenschaft)

Das Festlegen dieser Eigenschaft entspricht dem Festlegen der [transformsatsource-Richtlinien](transformsatsource-policy.md) Richtlinie, mit dem Unterschied, dass der Bereich abweicht. Das Festlegen der transformsatsource-Richtlinie gilt für alle Pakete, die von einem bestimmten Benutzer installiert wurden. Das Festlegen der **transformsatsource** -Eigenschaft gilt unabhängig von den Benutzern für das Paket.

## <a name="remarks"></a>Bemerkungen

Windows Installer interpretiert die **transformsatsource** -Eigenschaft so, als handele es sich um die [**transformssecure**](transformssecure.md) -Eigenschaft. Wenn das @-Flag in der [**Transformationen**](transforms.md) -Eigenschaft übermittelt wird, werden die Transformationen in der Liste von Windows Installer als [sichere Quell Transformationen](secure-at-source-transforms.md)behandelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 





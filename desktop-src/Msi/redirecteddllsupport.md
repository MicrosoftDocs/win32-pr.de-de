---
description: Der Installer legt die Eigenschaft redirecteddllsupport fest, wenn die Systemplattform, die die Installation ausführt, isolierte Komponenten unterstützt.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Redirecteddllsupport (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354204"
---
# <a name="redirecteddllsupport-property"></a>Redirecteddllsupport (Eigenschaft)

Der Installer legt die Eigenschaft **redirecteddllsupport** fest, wenn die Systemplattform, die die Installation ausführt, [isolierte Komponenten](isolated-components.md)unterstützt.

Der Installer legt die Eigenschaft **redirecteddllsupport** auf den Wert 1 fest, wenn das System, das die Installation ausführt, [isolierte Komponenten](isolated-components.md) unterstützt, die auf basieren. Lokale Dateien. Der Installer legt die Eigenschaft **redirecteddllsupport** auf den Wert 2 fest, wenn das System, das die Installation ausführt, die Isolation mithilfe von unterstützt. Lokale Dateien oder Win32-Assemblys nebeneinander.

Die Eigenschaft **redirecteddllsupport** kann verwendet werden, um die [isolatecomponents-Aktion](isolatecomponents-action.md) in der Tabelle [InstallUISequence](installuisequence-table.md) oder der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)zu bedinieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 





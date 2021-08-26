---
description: Das Installationsprogramm legt die RedirectedDLLSupport-Eigenschaft fest, wenn die Systemplattform, die die Installation durchführt, isolierte Komponenten unterstützt.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: RedirectedDLLSupport-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24da5990645d4c27120c3a010cc517475ba6e706c2fb41d69a024d15ca524549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979320"
---
# <a name="redirecteddllsupport-property"></a>RedirectedDLLSupport-Eigenschaft

Das Installationsprogramm legt die **RedirectedDLLSupport-Eigenschaft** fest, wenn die Systemplattform, die die Installation [durchführt, isolierte Komponenten](isolated-components.md)unterstützt.

Das Installationsprogramm legt die **RedirectedDLLSupport-Eigenschaft** auf den Wert 1 fest, wenn das System, das die Installation [ausführt, isolierte Komponenten](isolated-components.md) basierend auf unterstützt. LOCAL-Dateien. Das Installationsprogramm legt die **RedirectedDLLSupport-Eigenschaft** auf den Wert 2 fest, wenn das System, das die Installation ausführt, die Isolation mithilfe von unterstützt. LOCAL-Dateien oder Win32-Assemblys.

Die **RedirectedDLLSupport-Eigenschaft** kann verwendet werden, um die [IsolateComponents-Aktion](isolatecomponents-action.md) in der [Tabelle InstallUISequence](installuisequence-table.md) oder in der [Tabelle InstallExecuteSequence zu konditionieren.](installexecutesequence-table.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




